# Distilled

## Bert Distilled

1. [**DeFINE: DEep Factorized INput Word Embeddings for Neural Sequence Modeling**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Distilled/DEFINE.pdf) [ICLR 2020] _Sachin Mehta, Rik Koncel-Kedziorski, Mohammad Rastegari, Hannaneh Hajishirzi_.
   - reduce the input and output embed size.
   - add one multi-layer FC to improve the representation.
   - for getting multi-grain representation(dense and sparse), design one HGT architecture.
   - split and mixed group representation to residual connections.
2. [**TinyBERT: Distilling BERT for Natural Language Understanding**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/BertDistilled/TinyBert.pdf) [-] _Xiaoqi Jiao, Yichun Yin, Lifeng Shang, Xin Jiang, Xiao Chen, Linlin Li, Fang Wang, Qun Liu_.
   - New Two-stage distilling framework
     - pre-training Distillations
     - task-specific Distillations
   - Multi-grain distilling
     - Transformer-layer Distillations
       - Attention distillations
       - Hidden Distillations
     - Embedding-layer Distillations
     - Prediction-layer Distillations
3. [**DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/BertDistilled/DistilBERT.pdf) [NIPS 2019] _Victor Sanh, Lysandre Debut, Julien Chaumond, Thomas Wolf_.
   - cross entropy loss Lce + masked language model Lmlm + cosine embedding loss Lcos
   - Triplet Loss combining language modeling, distillation and cosine-distance losses
   - can be deploy in device, like iphone 7
4. [**Multi-Stage Distillation Framework for Massive Multi-lingual NER**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/BertDistilled/TinyMBERT_Multi_lingual_NER_Distillation.pdf) [ACL 2020] _Subhabrata (Subho) Mukherjee, Ahmed Hassan Awadallah_.
   - Distillation -> BiLSTM
   - Hard + Soft teacher.
   - Layer Parma KL
   - stage-wise
   - gradual unfreeze.
5. [**MobileBERT: Task-Agnostic Compression of BERT by Progressive Knowledge Transfer**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Distilled/MobileBERT.pdf) [ACL 2020] _Zhiqing Sun, Hongkun Yu, Xiaodan Song, Renjie Liu, Yiming Yang, Denny Zhou_.
   - Motivation: low latency, less parameters, comparable performance and task-agnostic in mobile.
   - Reduce embedding size like ALBERT, and use one multi-channel CNN to increase the hidden dimension.
   - In each Transformer block, use two Linear to up/down dimension and increase/decrease parameters.
   - Study teacher model in three dimension, 1) classification result and embedding. 2) linear in each layer. 3) MHA
   - Three strategy to learn the distillation. 1) Joint. 2) Two-stage. one for learning the FFN & MHA and then learning classification and embedding. 3) learn the FFN & MHA from bottom to top each one layer.
   - The LayerNorm and Gelu are significantly inference the latency.
