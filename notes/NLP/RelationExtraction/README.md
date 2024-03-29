# Relation Extraction

1. [**Matching the Blanks: Distributional Similarity for Relation Learning**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/MatchingtheBlanks.pdf) [ACL 2019] _Livio Baldini Soares, Nicholas FitzGerald, Jeffrey Ling, Tom Kwiatkowski_.
   - How to solve relation extraction task by using BERT
   - three representation
     1. standard BERT
     2. add Position embed
     3. Entity Mark
   - three output
     1. CLS output
     2. Mention level pooling
     3. Mention start
   - random replace the Entity -> `[BLANK]`
   - negative sample
2. [**Inducing Relational Knowledge from BERT**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/InducingRelationfromBERT.pdf) [AAAI 2020] _Zied Bouraoui, Jose Camacho-Collados, Steven Schockaert_.
   - using the middle sentence to represent the relation of the pair.
   - choose one temperate to do the cloze task.
3. [**Entity-Relation Extraction as Multi-Turn Question Answering**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/REasMulti-turnQA.pdf) [ACL 2019] _Xiaoya Li, Fan Yin, Zijun Sun, Xiayu Li, Arianna Yuan, Duo Chai, Mingxin Zhou, Jiwei Li_.
   - Start-end + Multi-time => RL. The model also a pipeline model.
4. [**Twenty-ﬁve years of information extraction**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/25YearsIE.pdf) [NLE 2019] _Ralph Grishman_
   - From Three Corpus to introduce the problem and method in Information Extraction IE in past 25 years.
5. [**Improving Entity Linking by Modeling Latent Entity Type Information**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/ImprovingEntityLinkingbyModelingLatentEntityTypeInformation.pdf) [AAAI 2020] _Shuang Chen, Jinpeng Wang, Feng Jiang, Chin-Yew Lin_.
   - Improve the embedding by [MASK]
6. [**Relation of the Relations: A New Paradigm of the Relation Extraction Problem**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/RelationoftheRelations.pdf) [-] _Zhijing Jin, Yongyi Yang, Xipeng Qiu, Zheng Zhang_.
   - Focus on Relation of Relations, directly learn the entity pairs matrix instead of one by one.
   - Statistic the co-occurrence of relation pairs.
   - BioROR. -> GNN.
   - MultiRoR. -> Transformer.
7. [**Relation Extraction using Explicit Context Conditioning**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/RelationExtractionusingExplicitContextConditioning.pdf) [NAACL 2019] _Gaurav Singh, Parminder Bhatia_.
   - Motivation:
     1. Get two-hop link relation.
     2. Get long dependencies.
   - Insight:
     1. Build first-order relation scores based on bi-affine transformer.
     2. Build second-order relation scores based on conditional score (combine two first-order scores which have same item k). => This part should improve by using GCN or other graph embedding architecture.
     3. One efficient implement which reduce the second order time cost.
