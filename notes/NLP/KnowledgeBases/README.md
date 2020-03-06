# Knowledge Bases

1. [**K-BERT: Enabling Language Representation with Knowledge Graph**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/K-BERT.pdf) [AAAI 2020 Reject] _Weijie Liu, Peng Zhou, Zhe Zhao, Zhiruo Wang, Qi Ju, Haotang Deng, Ping Wang_.
   - change previous word embedding + TranE => add knowledge to sentence(Like annotations)
   - The change maybe have noisy in semantic. So add one mask.
   - The improvement of performance is little.
2. [**K-Adapter: Infusing Knowledge into Pre-Trained Models with Adapters**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/K-Adapter.pdf) [-] _Ruize Wang, Duyu Tang, Nan Duan, Zhongyu Wei, Xuanjing Huang, Jianshu ji, Guihong Cao, Daxin Jiang, Ming Zhou_.
   - Add some Dense between Transformer block in the Bert-like Architectures to Fine-tune in the downstream task.
   - Bert params freeze.
   - can parallelism.
   - Continue learning.
