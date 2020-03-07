# Interpretability

1. [**Exploring the Memorization-Generalization Continuum in Deep Learning**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Interpretabilit/PredictingDSusingDistantSupervisionFromSentiment.pdf) [-] _Chiyuan Zhang♮, Ziheng Jiang♮, Kunal Talwar, Michael C. Mozer_.
   - defined a indicators to measure the degree of generalization consistency score(C-score).
   - But C-score need many many test to get the empirically average.
   - So use cumulative binary training loss to proxy score(p=.864)
     - kernel density estimation on input and hidden representation.
   - the lower C-score data need lower learning rate.
