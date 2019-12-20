# Bert Distilled

1. [**TinyBERT: Distilling BERT for Natural Language Understanding**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/BertDistilled/TinyBert.pdf) [-] _Xiaoqi Jiao, Yichun Yin, Lifeng Shang, Xin Jiang, Xiao Chen, Linlin Li, Fang Wang, Qun Liu_.
   - New Two-stage distilling framework
     - pre-training Distillations
     - task-specific Distillations
   - Multi-grain distilling
     - Transformer-layer Distillations
       - Attention distillations
       - Hidden Distillations
     - Embedding-layer Distillations
     - Prediction-layer Distillations
2. [**DistilBERT, a distilled version of BERT: smaller, faster, cheaper and lighter**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/BertDistilled/DistilBERT.pdf) [NIPS 2019] _Victor Sanh, Lysandre Debut, Julien Chaumond, Thomas Wolf_.
   - cross entropy loss Lce + masked language model Lmlm + cosine embedding loss Lcos
   - Triplet Loss combining language modeling, distillation and cosine-distance losses
   - can be deploy in device, like iphone 7
