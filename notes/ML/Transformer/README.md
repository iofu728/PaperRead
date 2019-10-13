# Transformer

1. [**On Layer Normalization IN The Transformer A Rchitecture**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/LayerNormTransformer.pdf) [submit ICLR 2020] _anonymous authors_.
   - the reason of post-LN Transformer needing warm-up process in theoretically and empirically.
   - The Position of Layer Normalization in residual connections is significant.
   - $\left\|\frac{\partial \tilde{\mathcal{L}}}{\partial W^{2, L}}\right\|_{F} \leq \mathcal{O}(d \sqrt{\ln d})$
   - $\left\|\frac{\partial \tilde{\mathcal{L}}}{\partial W^{2, L}}\right\|_{F} \leq \mathcal{O}(d \sqrt{\frac{\ln d}{L}})$
2. [**Understanding and Improving Transformer From a Multi-Particle Dynamic System Point of View**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/MacaronNet.pdf) [-] _Yiping Lu, Zhuohan Li, Di He, Zhiqing Sun,Bin Dong, Tao Qin, Liwei Wang, Tie-Yan Liu_.
   - Transformer is Ordinary Differential Equation ODE
   - And change Transformer architecture to FFN-Attention-FFN
3. [**Large Memory Layers with Product Keys**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/LargeMemoryLayers.pdf) [-] _Guillaume Lample, Alexandre Sablayrolles, Marc'Aurelio Ranzato, Ludovic Denoyer, Hervé Jégou_.
   - a network about key-value memory layer instead of FC in Transformer
   - It can reduce computational complexity.
4. [**A Tensorized Transformer for Language Modeling**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/TensorizedTransformer.pdf) [NIPS 2019] _Xindian Ma, Peng Zhang, Shuai Zhang, Nan Duan, Yuexian Hou, Dawei Song, Ming Zhou_.
   - parameters sharing + tensor decomposition
   - block-term tensor decomposition(BTD)
   - Multi-linear Attention by BTD
   - reduce computational complexity
5. [**Adaptive Attention Span in Transformers**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/AdaptiveAttSpanInTransformer.pdf) [ACL 2019] _Sainbayar Sukhbaatar, Edouard Grave, Piotr Bojanowski, Armand Joulin_.
   - adaptive attention span size reduce unnecessary cost.
   - origin Attention span $\in [t-S, t)$
   - In fact, diff head have diff focus. Maybe focus on near info, maybe on global info.
   - proposal a masking function to control attention span.
   - $m_{z}(x)=\min \left[\max \left[\frac{1}{R}(R+z-x), 0\right], 1\right]$
   - $a_{t r}=\frac{m_{z}(t-r) \exp \left(s_{t r}\right)}{\sum_{q=t-S}^{t-1} m_{z}(t-q) \exp \left(s_{t q}\right)}$
6. [**Universal Transformers**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/UniversalTransformers.pdf) [ICLR 2019] _Mostafa Dehghani, Stephan Gouws, Oriol Vinyals, Jakob Uszkoreit, Łukasz Kaiser_.
   - Recurrent Architectures -> time loop
   - Transition functions -> share parameters
   - adaptive computational time -> dynamic adjust step time
