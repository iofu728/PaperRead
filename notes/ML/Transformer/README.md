# Transformer

1. [< On Layer Normalization IN The Transformer A Rchitecture>](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/LayerNormTransformer.pdf) [submit ICLR 2020]
   - the reason of post-LN Transformer needing warm-up process in theoretically and empirically.
   - The Position of Layer Normalization in residual connections is significant.
   - $\left\|\frac{\partial \tilde{\mathcal{L}}}{\partial W^{2, L}}\right\|_{F} \leq \mathcal{O}(d \sqrt{\ln d})$
   - $\left\|\frac{\partial \tilde{\mathcal{L}}}{\partial W^{2, L}}\right\|_{F} \leq \mathcal{O}(d \sqrt{\frac{\ln d}{L}})$
2. [< Understanding and Improving Transformer From a Multi-Particle Dynamic System Point of View >](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/MacaronNet.pdf)
   - Transformer is Ordinary Differential Equation ODE
   - And change Transformer architecture to FFN-Attention-FFN
