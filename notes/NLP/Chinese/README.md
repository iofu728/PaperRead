# Chinese

1. [**NEZHA: Neural Contextualized Representation for Chinese Language Understanding**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Chinese/NeZha.pdf) [-] _Junqiu Wei, Xiaozhe Ren, Xiaoguang Li, Wenyong Huang, Yi Liao, Yasheng Wang, Jiashu Lin, Xin Jiang, Xiao Chen, Qun Liu_.
   - Bert in chinese corpus
   - change position -> relative position
   - using jieba to do the word segmentation
   - using mixing precision traning + LAMB optimizer
2. [**SpellGCN: Incorporating Phonological and Visual Similarities into Language Models for Chinese Spelling Check**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Chinese/SpellGCN.pdf) [ACL 2020] _Xingyi Cheng, Weidi Xu, Kunlong Chen, Shaohua Jiang, Feng Wang, Taifeng Wang, Wei Chu, Yuan Qi_.
   - In chinese spelling check task, there are lot of error due to phonological.
   - If only use the PLMs, we can get one semantic good result, but not for one which follow with the same phonological.
   - Inject the phonological information, but not for explicit.
   - They use one GCN base on BERT embeddings to do the random walk in a chinese confusing set like homophones, synonym.
   - After 3 GCN layers, we get the GCN output and the BERT encoder output.
   - Unlike MLM, the build the linear layer weight base on GCN embedding and BERT Encoder output which use in the vocab not in the GCN vocab set.
