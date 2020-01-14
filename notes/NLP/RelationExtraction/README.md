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
