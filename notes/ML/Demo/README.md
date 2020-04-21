# Demo

1. [**Transformers: State-of-the-art Natural Language Processing**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Demo/Transformers.pdf) [-] _Thomas Wolf, Lysandre Debut, Victor Sanh, Julien Chaumond, Clement Delangue, Anthony Moi, Pierric Cistac, Tim Rault, Rémi Louf, Morgan Funtowicz, Jamie Brew_.
   - Unified API for Bertology
   - Existing!!! Huggingface support ctrl in yesterday. It's so quick.
2. [**Comprehend Medical: a Named Entity Recognition and Relationship Extraction Web Service**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Demo/ComprehendMedical.pdf) [ICMLA 2019] _Parminder Bhatia, Busra Celikkaya, Mohammed Khalilia, Selvan Senthivel_.
   - NER + Relation Extraction API in AWS
3. [**Stanza: A Python Natural Language Processing Toolkit for Many Human Languages**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Demo/Stanza.pdf) [-] _Peng Qi, Yuhao Zhang, Yuhui Zhang, Jason Bolton, Christopher D. Manning_.
   1. Support 66 languages(Except NER, NER only support 8 languages). Not cross-lingual only is multi-lingual which means you should assign the language you used.
   2. For different tasks, it only uses a pipeline to independently train, rather than multi-task.
      1. Detail in https://arxiv.org/pdf/1901.10457.pdf
      2. NER
         1. BiLSTM + BiLSTM + CRF
   3. Toolkit native support python and also support java.
      a. RESTful APIs.
      b. HeartBeat
   4. The NER Corpus.
      a. AQMAR - Arabic
      b. OntoNotes 5.0: English, Chinese, Arabic(no use)
      c. CoNLL02: Dutch, Spanish
      d. WikiNER: German, Dutch, French, Russian, [English, Spanish, Italian, Portuguese(no use)]
      e. CoNLL03: English, German
      f. GermEval14: German
      g. AnCora: Spanish, Catalan(no use)
