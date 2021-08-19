# PLM Compression

## Transformer Compression

1. [**An Efficient Transformer Decoder with Compressed Sub-layers**](https://arxiv.org/pdf/2101.00542.pdf) [AAAI 20] _Yanyang Li, Ye Lin, Tong Xiao, Jingbo Zhu_.
   - In Decoder layer, parallel two attentions.
   - And remove FFN.

## Pruning

1. [**Movement Pruning: Adaptive Sparsity by Fine-Tuning**](https://arxiv.org/abs/2005.07683) [NeurIPS 20] _Victor Sanh, Thomas Wolf, Alexander M. Rush_.
   - Motivation: Magnitude 0-order method work on trained model, but for pretrained model which need fine-tune, it's not suitable.
   - The output is $\mathbf{a}=(\mathbf{W} \odot \mathbf{M}) \mathbf{x}$
   - $Top_v(S) \in \{0, 1\}$, use straight-through method to gradient.
   - The loss gradients should be $\frac{\partial \mathcal{L}}{\partial S_{i, j}}=\frac{\partial \mathcal{L}}{\partial a_{i}} \frac{\partial a_{i}}{\partial S_{i, j}}=\frac{\partial \mathcal{L}}{\partial a_{i}} W_{i, j} x_{j}$

## Embedding Compression

1. [**Compressing Word Embeddings via Deep Compositional Code Learning**](https://arxiv.org/pdf/1711.01068.pdf) [ICLR 18] _Raphael Shu, Hideki Nakayama_.
   - The first one propose Code-based Methods to slove embedding compression problem.
   - To find the basic vector from word embedding space, and use it(the number << the vocabular size) to represent other embeddings.
   - Use Gumbel Softmax to reparameter.
2. [**Near-lossless Binarization of Word Embeddings**](https://arxiv.org/pdf/1803.09065.pdf) [AAAI 2019] _Julien Tissier, Christophe Gravier, Amaury Habrard_.
   - AutoEncoder to Binarization embedding. somehow oneway of code-based methods.
3. [**Improving Word Embedding Factorization for Compression Using Distilled Nonlinear Neural Decomposition**](https://arxiv.org/pdf/1910.06720.pdf) [EMNLP 20 Finding] _Vasileios Lioutas, Ahmad Rashid, Krtin Kumar, Md Akmal Haidar, Mehdi Rezagholizadeh_.
   - KD + Matrix Decompose
4. [**Adaptive Compression of Word Embeddings**](https://aclanthology.org/2020.acl-main.364.pdf) [ACL 20] _Yeachan Kim, Kang-Min Kim, SangKeun Lee_.
   - Adpative Code-Based Model.
