# Attack

1. [**Weight Poisoning Attacks on Pre-trained Models**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Attack/RIPPLe.pdf) [ACL 2020] _Keita Kurita, Paul Michel, Graham Neubig_.
   - change PLMs weight to attack classification result even if after finetune, and not need know the downstream knowledge.
   - one is base on two part optimization.
   - one is base on mean pooling the co-occurrence token embeddings.
