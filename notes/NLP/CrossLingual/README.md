# Cross-Lingual

1. [**Enhanced Meta-Learning for Cross-lingual Named Entity Recognition with Minimal Resources**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/Cross-lingualNER.pdf) [AAAI 2020] _Qianhui Wu, Zijia Lin, Guoxin Wang, Hui Chen, Börje F. Karlsson, Biqing Huang, Chin-Yew Lin_.
   - Motivation: direct transfer can't have a good performance, if we use the most similar k sample to fine-tune the source model.
   - k sample is low-sample learning so use the meta-learning.
   - To find the language-independent features mask entity to predict.
   - average loss reflect the high loss token can't influence loss so add the supplement max loss.
   - low-resource.
2. [**XTREME: A Massively Multilingual Multi-task Benchmark for Evaluating Cross-lingual Generalization**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/CrossLingual/XTREME.pdf) [-] _Junjie Hu, Sebastian Ruder, Aditya Siddhant, Graham Neubig, Orhan Firat, Melvin Johnson_.
   - Multi-task Cross-lingual benchmark.
3. [**Unicoder: A Universal Language Encoder by Pre-training with Multiple Cross-lingual Tasks**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/CrossLingual/Unicoder.pdf) [EMNLP 2019] _Haoyang Huang, Yaobo Liang, Nan Duan, Ming Gong, Linjun Shou, Daxin Jiang, Ming Zhou_.
   - crosslingual word recovery
   - cross-lingual paraphrase classiﬁcation
   - cross-lingual masked language model
