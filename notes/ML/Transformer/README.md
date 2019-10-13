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
