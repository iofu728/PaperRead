# Model Compression

## Transformer Compression

1. [**An Efficient Transformer Decoder with Compressed Sub-layers**](https://arxiv.org/pdf/2101.00542.pdf) [AAAI 20] _Yanyang Li, Ye Lin, Tong Xiao, Jingbo Zhu_.
   - In Decoder layer, parallel two attentions.
   - And remove FFN.

## Pruning

### Workshop

1. [**NeurIPS 2021 ENSLP Workshop**](https://neurips2021-nlp.github.io/) Efficient Natural Language and Speech Processing(Models, Training and Inference)

### Normal Pruning

1. [**Movement Pruning: Adaptive Sparsity by Fine-Tuning**](https://arxiv.org/abs/2005.07683) [NeurIPS 20] _Victor Sanh, Thomas Wolf, Alexander M. Rush_.
   - Motivation: Magnitude 0-order method work on trained model, but for pretrained model which need fine-tune, it's not suitable.
   - The output is $\mathbf{a}=(\mathbf{W} \odot \mathbf{M}) \mathbf{x}$
   - $Top_v(S) \in \{0, 1\}$, use straight-through method to gradient.
   - The loss gradients should be $\frac{\partial \mathcal{L}}{\partial S_{i, j}}=\frac{\partial \mathcal{L}}{\partial a_{i}} \frac{\partial a_{i}}{\partial S_{i, j}}=\frac{\partial \mathcal{L}}{\partial a_{i}} W_{i, j} x_{j}$

### Head Pruning

1. [**SpAtten: Efficient Sparse Attention Architecture with Cascade Token and Head Pruning**](https://arxiv.org/abs/2012.09852).[HPCA21] _Hanrui Wang, Zhekai Zhang, Song Han_. [Hardware-Software]
   a. Cascade(Iterative, deeper, more sparse) Token and Head pruning.
   b. Magnitude-base/Important-base.
   c. Top-K engine
2. [**Pruning Attention Heads of Transformer Models Using A\* Search: A Novel Approach to Compress Big NLP Architectures**](https://arxiv.org/abs/2110.15225). _Archit Parnami, Rahul Singh, Tarun Joshi_. [Sensitivity-base]
   a. A\*, loss-based
3. [**Differentiable Subset Pruning of Transformer Heads**](https://arxiv.org/abs/2108.04657). [TACL21]. _Jiaoda Li, Ryan Cotterell, Mrinmaya Sachan_.[Gradient-base]
   a. Gumble-Tok-K, gradient-based, both in pipeline mode & joint pruning mode.
4. [**Are Sixteen Heads Really Better than One?**](https://arxiv.org/abs/1905.10650)[NeurIPS19]. _Paul Michel, Omer Levy, Graham Neubig_.[Sensitivity-base]
   a. Sensitivity-base, Iterative,
5. [**Analyzing Multi-Head Self-Attention: Specialized Heads Do the Heavy Lifting, the Rest Can Be Pruned**](https://arxiv.org/abs/1905.09418). [ACL19]. _Elena Voita, David Talbot, Fedor Moiseev, Rico Sennrich, Ivan Titov_.[Gradient-base]
   a. Stochastic gates with Hard Gumbel-Softmax distrubtion.
6. [**Scheduled DropHead: A Regularization Method for Transformer Models**](https://arxiv.org/abs/2004.13342). [EMNLP20 Finding]. _Wangchunshu Zhou, Tao Ge, Ke Xu, Furu Wei, Ming Zhou_.
   a. Dropout Head to prevent the multi-head attention model from being dominated by a small portion of attention heads.

### Layer Pruning

1. [**Reducing Transformer Depth on Demand with Structured Dropout**](https://openreview.net/forum?id=SylO2yStDr). [ICLR20]. _Angela Fan, Edouard Grave, Armand Joulin_. [DropConnect]
   a. Add Layer-level DropConnect in training processing.

### Transfomer Pruning

1. [**Compressing Large-Scale Transformer-Based Models: A Case Study on BERT**](https://arxiv.org/abs/2002.11985). [TACL21]. _Prakhar Ganesh, Yao Chen, Xin Lou, Mohammad Ali Khan, Yin Yang, Hassan Sajjad, Preslav Nakov, Deming Chen, Marianne Winslett_. [Survey]
   a. Unstructure Pruning: Magnitude, Movement， Rewrited Proximal PruningRPP()
   b. Structure: Head, Layer, Embedding Layer.
   c. Matrix decomposition.
2. [**Compressing BERT: Studying the Effects of Weight Pruning on Transfer Learning**](https://arxiv.org/abs/2002.08307).[ACL20 Workshop Rep4NLP] _Mitchell A. Gordon, Kevin Duh, Nicholas Andrews_. [Magnitude-base]
   a. Does compressing BERT impede it’s ability to transfer to new tasks?Does fine-tuning make BERT more or less compressible?
   b. Low levels of pruning (30-40%) are ok. Medium levels/High levels of pruning weak performance downstream tasks.
   c. Finally, we observe that fine-tuning BERT on a specific task does not improve its prunability or change the order of pruning by a meaningful amount.
3. [**Train Large, Then Compress: Rethinking Model Size for Efficient Training and Inference of Transformers**](https://arxiv.org/abs/2002.11794). [ICML20]. _Zhuohan Li, Eric Wallace, Sheng Shen, Kevin Lin, Kurt Keutzer, Dan Klein, Joseph E. Gonzalez_. [Iterative Magnitude-base]
   a. Deeper, more wide model with pruning better than small model.
4. [**Structured Pruning of Large Language Models**](https://arxiv.org/abs/1910.04732). [EMNLP20]. _Ziheng Wang, Jeremy Wohlwend, Tao Lei_. [Factorized Structure Pruning]
   a. Factorized low-rank pruning.
5. [**Structured Pruning of a BERT-based Question Answering Model**](https://arxiv.org/abs/1910.06360). _J.S. McCarley, Rishav Chakravarti, Avirup Sil_.[weight-base]
   a. using L0 to structure pruning.
6. [**Block Pruning For Faster Transformers**](https://arxiv.org/abs/2109.04838). [EMNLP21]. _François Lagunas, Ella Charlaix, Victor Sanh, Alexander M. Rush_. [Gradient-base]
   a. Hybird-filled Movement Pruning.
7. [**MLPruning: A Multilevel Structured Pruning Framework for Transformer-based Models**](https://arxiv.org/abs/2105.14636). _Zhewei Yao, Linjian Ma, Sheng Shen, Kurt Keutzer, Michael W. Mahoney_. [Gradient-base]
   a. Multi-stage, different regulation to contrul ununiform.
8. [**NViT: Vision Transformer Compression and Parameter Redistribution**](https://arxiv.org/abs/2110.04869). _Huanrui Yang, Hongxu Yin, Pavlo Molchanov, Hai Li, Jan Kautz_. [Vision, Gradient-base]
   a. Structure first-order Talyor pruning.
9. [**Layer-wise Model Pruning based on Mutual Information**](https://arxiv.org/abs/2108.12594). [EMNLP21]. _Chun Fan, Jiwei Li, Xiang Ao, Fei Wu, Yuxian Meng, Xiaofei Sun_. [MI]
   a. Top-down Iterative pruning base on mutual information.
10. [**Rethinking Network Pruning-under the Pre-train and Fine-tune Paradigm**](https://arxiv.org/abs/2104.08682). _Dongkuan Xu, Ian E.H. Yen, Jinxi Zhao, Zhibin Xiao_. [Magnitude-base]
11. [**TPrune: Efficient Transformer Pruning for Mobile Devices**](https://dl.acm.org/doi/abs/10.1145/3446640). [TCPS21]. _Jiachen Mao, Huanrui Yang, Ang Li, Hai Li, Yiran Chen_. [Regulation-base]
    a. Using block-wise structure sprity pruning(BSSL) only train with regulation, find that WQ, WK, WV, WFFN1 are colum-wise, WO, WFFN2 are row-wise. WQ, WK, WV are pruned at some extent. Wo, WFFN1, WFFN2 hardly get sparity. Different layer in encode-decode should set different sparity ratio.
    b. propose one method base on Structured Hoyer Square(also in regulation-base).
12. [**LadaBERT: Lightweight Adaptation of BERT through Hybrid Model Compression**](https://arxiv.org/abs/2004.04124). [Coling20]. _Yihuan Mao, Yujing Wang, Chufan Wu, Chen Zhang, Yang Wang, Yaming Yang, Quanlu Zhang, Yunhai Tong, Jing Bai_.
    a. Weight pruning + SVD + KD
13. [**Reweighted Proximal Pruning for Large-Scale Language Representation**](https://arxiv.org/abs/1909.12486). _Fu-Ming Guo, Sijia Liu, Finlay S. Mungall, Xue Lin, Yanzhi Wang_. [Prominal-Pruning]
    a. Reweighted L1, to avoid bigger |wi| get much more gradient than small wj.
    b. Using prominal to learn the L1.
14. [**EarlyBERT: Efficient BERT Training via Early-bird Lottery Tickets**](https://arxiv.org/abs/2101.00063). [ACL21]. _Xiaohan Chen, Yu Cheng, Shuohang Wang, Zhe Gan, Zhangyang Wang, Jingjing Liu_. [Magnitude-base structured]
    a. RPP + Magnitude-base structured + lottery tickets.
15. [**Chasing Sparsity in Vision Transformers: An End-to-End Exploration**](https://arxiv.org/abs/2106.04533). [NeurIPS21]. _Tianlong Chen, Yu Cheng, Zhe Gan, Lu Yuan, Lei Zhang, Zhangyang Wang_. [ViT + Iterative Taylor]
    a. Token Pruning + Iterative structured Taylor Attention head pruning + L1 FFN Pruning.
16. [**Aligned Weight Regularizers for Pruning Pretrained Neural Networks**](https://openreview.net/pdf?id=8Gd6ZzHJG5C). [ARR21Nov]. [Magnitude-base]
    a. Using a regulator loss to align pruned weight and origin weight, like cosine-base and frobenius-base.

### Token Pruning or Sparse Attention

1. [**Adaptively Sparse Transformers**](https://arxiv.org/abs/1909.00015). [EMNLP 2019]. _Gonçalo M. Correia, Vlad Niculae, André F.T. Martins_.
   a. α-entmax, which replace softmax in attention.
2. [**Blockwise Self-Attention for Long Document Understanding**](https://arxiv.org/abs/1911.02972). [EMNLP20 Finding]. _Jiezhong Qiu, Hao Ma, Omer Levy, Scott Wen-tau Yih, Sinong Wang, Jie Tang_.[hand-craft-base]
   a. Block Attntion Pruning, but only have N=2/3 two pattern.
3. [**Learned Token Pruning for Transformers**](https://arxiv.org/abs/2107.00910). _Sehoon Kim, Sheng Shen, David Thorsley, Amir Gholami, Woosuk Kwon, Joseph Hassoun, Kurt Keutzer_. [Token Pruning, gradient-base]
   a. Input sequence lengths can vary greatly within tasks and between training and validation sets, and thus a single pruning configuration can potentially under- prune shorter sequences or over-prune longer sequences.
   b. Straight-Through Estimator binarized mask.
4. [**PoWER-BERT: Accelerating BERT Inference via Progressive Word-vector Elimination**](https://arxiv.org/abs/2001.08950). [ICML20]. _Saurabh Goyal, Anamitra R. Choudhury, Saurabh M. Raje, Venkatesan T. Chakaravarthy, Yogish Sabharwal, Ashish Verma_. [Cascade Token Pruning]
5. [**Length-Adaptive Transformer: Train Once with Length Drop, Use Anytime with Search**](https://arxiv.org/abs/2010.07003). [ACL21]. _Gyuwan Kim, Kyunghyun Cho_. [Token Pruning]
   a. LengthDrop with trade-off search to find a model suit performance & efferient requirments.
   b. Drop-and-Restore make method can use in generator/MRC tasks.
6. [**TR-BERT: Dynamic Token Reduction for Accelerating BERT Inference**](https://arxiv.org/abs/2105.11618). [NAACL21]. _Deming Ye, Yankai Lin, Yufei Huang, Maosong Sun_. [RL + Token Pruning]
   a. RL to decide layer by layer.

### MoE

1. [**A Mixture of h−1 Heads is Better than h Heads**](https://arxiv.org/abs/2005.06537). [ACL20]. _Hao Peng, Roy Schwartz, Dianqi Li, Noah A. Smith_.
   a. MoE for Attention.
2. [**EBERT: Efficient BERT Inference with Dynamic Structured Pruning**](https://aclanthology.org/2021.findings-acl.425/). [ACL21 Finding]. _Zejian Liu, Fanrong Li, Gang Li, Jian Cheng_.
   a. Using a model(FFN + BN) to router structured weight(head-level in MHA, channel-level in FFN)

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
