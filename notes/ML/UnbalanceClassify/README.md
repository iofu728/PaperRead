# Unbalance Classify

1. [**Class-Balanced Loss Based on Effective Number of Samples**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/InBalanceClassify/Class-BalancedLoss.pdf) [CVPR 2019] _Yin Cui, Menglin Jia, Tsung-Yi Lin, Yang Song, Serge Belongie_.
   - a novel sample method using in loss calculate to solve unbalance problem.
   - Two proposition about effective number of sample
     - $E_{n}=\left(1-\beta^{n}\right) /(1-\beta)$, where $\beta=(N-1)/N$
     - $$E_{n}=\left(1-\beta^{n}\right) /(1-\beta)=\sum_{j=1}^{n} \beta^{j-1}$$
     - N more, $\beta$ -> 1; N=1, $\beta$ -> 0
   - use in softMax cross entropy, sigmoid, focal loss
