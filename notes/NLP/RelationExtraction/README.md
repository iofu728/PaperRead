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
