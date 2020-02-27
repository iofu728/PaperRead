# Optimization

1. [**Adam: A Method for Stochastic Optimization**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Optimization/Adam.pdf) [ICLR 2015] _Diederik P. Kingma, Jimmy Ba_.
   - Momentum(Exponential weighted average) + squared gradient.
   - first-order gradient.
   - Due to $g_t < g_{t-i}$. So, the weight of history gradient is higher than before.
   - It also eased the excessively fast gradient descent originally brought by squared gradient and speed up the slow gradient descent.
