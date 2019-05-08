# ConvS2S

[Convolutional Sequence to Sequence Learning](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Summarization/ConvS2S.pdf)

![image](https://cdn.nlark.com/yuque/0/2019/png/104214/1557313940009-50533623-d8c6-4b49-85d7-f0c4c8438fe9.png)

- Summarization
- Position Embedding
- Convolutional Layer

  - 非线性一维卷积层 窗口 k
  - 非线性结构能获得全局信息和局部信息
  - GLU - no-line gating mechanism
    - A similar nonlinearity has been introduced in Oord et al. (2016b) who apply tanh to A but Dauphin et al. (2016) shows that **GLUs** perform better in the context of language modelling.
    - $v([A B])=A \otimes \sigma(B)$
  - To enable deep convolutional networks, we add **residual connections** from the input of each convolution to the output of the block (He et al., 2015a).
  - $h_{i}^{l}=v\left(W^{l}\left[h_{i-k / 2}^{l-1}, \ldots, h_{i+k / 2}^{l-1}\right]+b_{w}^{l}\right)+h_{i}^{l-1}$
  - Need **Padding** to ensure output len same
    - Special, k - 1 pad in left & right in Input Layer; And remove k pad in Output Layer.
  - **linear mappings** between embedding size f and the convolution outputs that are of size 2d.
  - **Another**, (Embedding + Encoder output -> using Transform -> Decoder). apply such a transform to w when feeding embedding to the encoder network, to the encoder output $z_j^u$ , to the final layer of the decoder just before the softMax $h^L$ , and to all decoder layers $h^l$ before computing attention scores.
  - $p\left(y_{i+1} | y_{1}, \ldots, y_{i}, \mathbf{x}\right)=\operatorname{softmax}\left(W_{o} h_{i}^{L}+b_{o}\right) \in \mathbb{R}^{T}$

- Multi-step Attention
  - combine the current decoder state $h_i^l$ with an embedding of the previous target element $g_i$, $d_{i}^{l}=W_{d}^{l} h_{i}^{l}+b_{d}^{l}+g_{i}$
  - 注意力分布使用了点积方式**`Dot Product`**: decoder state summary $d_i^l$ and each output $z_j^u$ of the last encoder block u: $a_{i j}^{l}=\frac{\exp \left(d_{i}^{l} \cdot z_{j}^{u}\right)}{\sum_{t=1}^{m} \exp \left(d_{i}^{l} \cdot z_{t}^{u}\right)}$
  - 然后对获得的注意力分布做加权平均 $c_{i}^{l}=\sum_{j=1}^{m} a_{i j}^{l}\left(z_{j}^{u}+e_{j}\right)$
  - 在做加权平均的过程中，加了$e_j$, 类似于 [key-value 记忆网咯](https://arxiv.org/pdf/1606.03126.pdf) key-$z_j^U$, value - $z_j^u+e_j$
  - 在语义含义中，$z_j^u$表示的是 大量上下文的信息，$e_j$表示的是点状局部的信息
  - 还使用了多步的注意力机制，每层的 Attention 输出会作为输入给到下一层 Attention 中
  - decoder 中，每一步也包含了前 k-1 步的信息，因为$c_{i-k}^{l-1}$是$h_j$的一部分
  - 然后把获得的结果结合进入 CNN
- 归一化策略
  - 在训练过程中，通过细致的权值初始化 & 扩展网络结构 来保证网络变量不会发生突变
  - 令残差块输出项与 Attention 输出项大小一致，使得能保存激活的变量。
  - 将输出和输入的残差块之和乘上$\sqrt{0.5}$，使得参数之和减半。
  - 注意到$c_{i}^{l}=\sum_{j=1}^{m} a_{i j}^{l}\left(z_{j}^{u}+e_{j}\right)$ 是 m 个向量之和，为了抵消它的影响，乘上了$m \sqrt{1 / m}$
  - 放大输入到 m 倍，假设输入是均匀分布
  - 对卷积 decoder 层的梯度也做了一个缩放，使得能够更稳定的学习
- 参数初始化
  - 当不同层做归一化激活项的时候（比如说残差连接），需要 careful 的初始化参数
  - Motivation: 通过前向 & 后向传播，来维持激活的变量
  - EMbedding 初始化为一个正态分布，均值 0, 方差 0.1
  - 输出并不是直接喂给 GLU(gated linear unit), 而是 初始化一个权值$\mathcal{N}\left(0, \sqrt{1 / n_{l}}\right)$，其中$n_{l}$是输入层的神经元连接数
  - 在 GLU 激活层之后，文章用了一个 适应推到过程 [adapting the derivations](http://proceedings.mlr.press/v9/glorot10a/glorot10a.pdf) 的 scheme
  - 如果 GLU 输入分布是一个均值为 0，偏差较小的分布，则可以输出偏差可以用输入偏差的 1/4 来估计
  - 因此在初始化的时候构造一个 GLU 激活层的输入使得，偏差等于输出的 4 倍
  - 然后还对输入层做了一个 dropout 的操作 使得总体的概率在 p 左右
  - dropout 使得参数量减少了 1/p
  - 利用各自初始化 用大量参数维护变量值的稳定
  - 如果输出是 GLU 的一个子项$\mathcal{N}\left(0, \sqrt{4 p / n_{l}}\right)$
  - 否则，则是$\mathcal{N}\left(0, \sqrt{p / n_{l}}\right)$
