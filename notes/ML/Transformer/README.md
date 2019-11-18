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
7. [**Depth-Adaptive Transformer**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/DepthAdaptiveTransformer.pdf) [submit ICLR 2020] _Maha Elbayad, Jiatao Gu, Edouard Grave, Michael Auli_.
   - depth adaptive Transformer
   - not enough every token run -> last layer
   - $$\forall n, p\left(y_{t+1} | h_{t}^{n}\right)=\operatorname{softmax}\left(W_{n} h_{t}^{n}\right)$$
   - disadvantages: O(N), classification sole.
   - origin method: dynamic calculate
     - Aligned Training: know 1~i-1 layers all hidden parameters
       - $$\mathrm{LL}_{t}^{n}=\log p\left(y_{t} | h_{t-1}^{n}\right), \quad \mathrm{LL}^{n}=\sum_{t=1}^{|\boldsymbol{y}|} \mathrm{LL}_{t}^{n}, \quad \mathcal{L}_{d e c}(\boldsymbol{x}, \boldsymbol{y})=-\frac{1}{\sum_{n} \omega_{n}} \sum_{n=1}^{N} \omega_{n} \mathrm{LL}^{n}$$
     - Mixed Training: i+1 copy i layer
       - $$\mathrm{LL}_{t}=\log p\left(y_{t} | h_{t-1}^{n}\right), \quad \mathrm{LL}=\sum_{t=1}^{|\boldsymbol{y}|} \mathrm{LL}_{t}, \quad \mathcal{L}_{\operatorname{dec}}(\boldsymbol{x}, \boldsymbol{y})=-\frac{1}{M} \sum_{m=1}^{M} \mathrm{LL}$$
   - Paper Method: Depth-Adaptive
     - Sequence-specific depth: the same sequence quit same time
       - likelihood-based
         - $$q^{*}(\boldsymbol{x}, \boldsymbol{y})=\delta\left(\arg \max _{n} \mathrm{LL}^{n}-\lambda n\right)$$
       - correctness-based
         - $$C^{n}=\#\left\{t\left|y_{t}=\arg \max _{y} p\left(y | h_{t-1}^{n}\right\}, \quad q^{*}(\boldsymbol{x}, \boldsymbol{y})=\delta\left(\arg \max _{n} C^{n}-\lambda n\right)\right.\right.$$
     - token-specific depth
       - Multinomial
       - Poisson Binomial
       - likelihood-based
         - $$\begin{array}{l}{\kappa\left(t, t^{\prime}\right)=e^{-\frac{\left|t-t^{\prime}\right|^{2}}{\sigma}}, \text { smoothLL }_{t}^{n}=\sum_{t^{\prime}} \kappa\left(t, t^{\prime}\right) \mathrm{LL}_{t^{\prime}}^{n}} \\ {q_{t}^{*}(\boldsymbol{x}, \boldsymbol{y})=\delta\left(\arg \max _{n} \operatorname{smooth} \mathrm{LL} \mathrm{L}_{t}^{n}-\lambda n\right)}\end{array}$$
       - correctness-based
         - $$\begin{array}{l}{C_{t}^{n}=y_{t}=\arg \max _{y} p\left(y | h_{t-1}^{n}\right), \operatorname{smooth} \mathrm{C}_{t}^{n}=\sum_{t^{\prime}} \kappa\left(t, t^{\prime}\right) C_{t}^{n}} \\ {q_{t}^{*}(\boldsymbol{x}, \boldsymbol{y})=\delta\left(\arg \max _{n} \operatorname{smooth} \mathrm{C}_{t}^{n}-\lambda n\right)}\end{array}$$
       - confidence threshold
8. [**Star-Transformer**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/StarTransformer.pdf) [NAACL 2019] _Qipeng Guo, Xipeng Qiu, Pengfei Liu, Yunfan Shao, Xiangyang Xue, Zheng Zhang_.
   - change the FFN architecture of Transformer to Star architecture
   - reduce the compute cost and the dataSet need.
