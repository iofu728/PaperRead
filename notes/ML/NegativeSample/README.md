# Negative Sample

1. [**Incorporating GAN for Negative Sampling in Knowledge Representation Learning**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/NegativeSample/IncorporatingGANforNegativeSamplinginKnowledgeRepresentationLearning.pdf) [AAAI 2018] _Peifeng Wang, Shuangyin Li, Rong pan_.
   - using GAN to generate high-quantity negative sample.
   - view origin model as reward
2. [**NSCaching: Simple and Efficient Negative Sampling for Knowledge Graph Embedding**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/NegativeSample/NSCaching.pdf) [ICDE 2019] _Yongqi Zhang, Quanming Yao, Yingxia Shao, Lei Chen_.
   - Using one dynamical strategy replace GAN to reduce vanishing gradient problem.
3. [**VSE-ens: Visual-Semantic Embeddings with Efficient Negative Sampling**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/NegativeSample/VSE-ens.pdf) [AAAI 2018] _Guibing Guo, Songlin Zhai, Fajie Yuan, Yuan Liu, Xingwei Wang_.
   - Dynamic Sampler to reduce the sample time in the later training period.
4. [**Negative Sampling in Variational Autoencoders**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/NegativeSample/NegativeSamplingInVariationalAutoencoders.pdf) [-] _Adrián Csiszárik, Beatrix Benkő, Dániel Varga_.
   - Negative Sampling in Variational Autoencoders
5. [**Knowledge Graph Embedding by Translating on Hyperplanes**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/NegativeSample/KnowledgeGraphEmbeddingbyTranslatingonHyperplanes.pdf) [AAAI 2014] _Zhen Wang, Jianwen Zhang, Jianlin Feng, Zheng Chen_.
   - Motivation: There are many-to-many pair in Entity Linking Problem.
   - 1.h+r-t => project in hyperplanes.
   - 2.Bernoulli Sample when dicide which entity will be replace (head or tail). reduce the probability of which entity is multi-label.
