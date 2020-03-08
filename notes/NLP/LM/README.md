# Language Models

## Knowledge Language Models

1. [**A Neural Knowledge Language Model**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/KnowledgeLM.pdf) [-] _Sungjin Ahn, Heeyoul Choi, Tanel Pärnamaa, Yoshua Bengio_.
   - add knowledge to Language Models.
   - Tuple(head entity, relation, tail entity).
   - token-level topic knowledge.
   - aligned knowledge.
2. [**Latent Relation Language Models**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/LatentRelationLM.pdf) [AAAI 2020] _Hiroaki Hayashi*, Zecong Hu*, Chenyan Xiong, Graham Neubig_.
   - Span-level.
   - Aligned entity to raw text by latent parameters.
     - span variable
     - source variable
     - relation variable

## Contextual Word Representation

1. [**Contextual Word Representations: A Contextual Introduction**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/ContextualWordRepresentations.pdf) [-] _Noah A. Smith_.
   - Survey of Contextual Word Representations

## Parallelism

1. [**Megatron-LM: Training Multi-Billion Parameter Language Models Using GPU Model Parallelism**](https://github.com/iofu728/PaperRead/blob/master/NLP/Parallelism/Megatron-LM.pdf) [-] _Mohammad Shoeybi, Mostofa Patwary Raul Puri, Patrick LeGresley, Jared Casper, Bryan Catanzaro_.
   - parallelism bert.
   - using Pre-LN Transformer instead of Post-LN Transformer in Origin Bert
   - using the GELU instead of RELU
   - little of code change in parallelism architecture.
