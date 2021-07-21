# SpeedUp

1. [LightSeq: A High Performance Inference Library for Transformers](https://arxiv.org/pdf/2010.13887) [NAACL 2021] _Xiaohui Wang, Ying Xiong, Yang Wei, Mingxuan Wang, Lei Li_.
   1. use rewrite kernel and CuBLAS GEMM; Save most of the time;
   2. Propose one hierarchical beam search method, which use retrieve-rerank two-stage to reduce the softmax calculate.
   3. Dynamic GPU memory reuse.
