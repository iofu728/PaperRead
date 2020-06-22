# Discourse Parsing

1. [**Predicting Discourse Structure using Distant Supervision from Sentiment**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Parsing/PredictingDSusingDistantSupervisionFromSentiment.pdf) [EMNLP 2019] _Patrick Huber, Giuseppe Carenini_.
   - In DP Task, the corpus is so small that NN method not work in this task.
   - But the annotated is very expensive, so need a method to generate the dataSet.
   - And the Discourse Parsing Task is a fundamental task in NLP which can be use by some downstream task like sentiment analysis.
   - So having a mind whether can use the sentiment info to generate the dataSet.
     1. Using a big sentiment to train a SOTA Sentiment Analyzer Model.
     2. Using the SOTA Hidden -> Generation CKY-style tree.
   - Evaluation in inter-domain corpus to prove the transfer info is useful.
2. [**Universal Dependency Parsing from Scratch**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Parsing/UniversalDependencyParsing.pdf) [CONLL 2018] _Peng Qi, Timothy Dozat, Yuhao Zhang, Christopher D. Manning_.
   - Tokenization, sentence split, Multi-word tokens split.
     - Predict a given character is the end of a token, end of a sentence, or end of a multiword token.
     - MWT example:
     - Input: four-dimensional binary feature vector as input,
       1. does the unit start with whitespace;
       2. does it start with a capitalized letter;
       3. is the unit fully capitalized;
       4. is it purely numerical.
     - Two layer BiLSTM, Three MLP
   - Expand MWT
     - Many languages, like German, have only a handful of rules for expanding a few MWTs.
     - First, look it up in the dictionary, and return the expansion recorded there if one can be found.
     - If this fails, we retry by lowercasing the incoming token.
     - If that fails again, we resort to the neural system to predict the ﬁnal expansion, which is a seq2seq base on LSTM + Bahdanau Attention model.
   - POS, UPOS
     - Input:
       1. pretrained word embedding, like word2vec, fastText.
       2. trainable frequent word embedding(frequent > 7)
       3. character-level embedding, base on LSTM.
     - BiLSTM + FC
     - Using biafﬁne attention.
   - Lemmatizer
     - Same as ②, diction + seq2seq
       1. exactly identical to the word (e.g., URLs and emails),
       2. the lowercased version of the word (e.g., capitalized rare words in English that are not proper nouns),
       3. Seq2seq
   - Dependency Parser
     1. Using the last token of multi-word as the word.
     2. Input:
        1. input pretrained word embeddings,
        2. frequent word and lemma embeddings,
        3. character-level word embeddings,
        4. summed XPOS and UPOS embeddings,
        5. summed UFeats embeddings.
     - BiLSTM + FC + Biaffine Attention
     - Add relation position information
3. [**Deep Biaffine Attention for Neural Dependency Parsing**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Parsing/biaffine.pdf) [ICLR 2017] _Timothy Dozat, Christopher D. Manning_.
   - graph-base method.
   - Matrix multiplication.
4. [**Perturbed Masking: Parameter-free Probing for Analyzing and Interpreting BERT**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Parsing/PerturbedMasking.pdf) [ACL 2020] _Zhiyong Wu, Yun Chen, Ben Kao, Qun Liu_.
   - Mask x\{x_i}.
   - d(x\{x_i}, x\{x_i, x_j}) => T\*T
