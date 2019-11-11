# Discourse Parsing

1. [**Predicting Discourse Structure using Distant Supervision from Sentiment**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/DiscourseParsing/PredictingDSusingDistantSupervisionFromSentiment.pdf) [EMNLP 2019] _Patrick Huber, Giuseppe Carenini_.
   - In DP Task, the corpus is so small that NN method not work in this task.
   - But the annotated is very expensive, so need a method to generate the dataSet.
   - And the Discourse Parsing Task is a fundamental task in NLP which can be use by some downstream task like sentiment analysis.
   - So having a mind whether can use the sentiment info to generate the dataSet.
   - 1. Using a big sentiment to train a SOTA Sentiment Analyzer Model.
   - 2. Using the SOTA Hidden -> Generation CKY-style tree.
   - Evaluation in inter-domain corpus to prove the transfer info is useful.
