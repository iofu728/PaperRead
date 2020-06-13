# Attention

1. [**Analyzing Multi-Head Self-Attention: Specialized Heads Do the Heavy Lifting, the Rest Can Be Pruned**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Attention/AnalysisMultiHeadAttention.pdf) [ACL 2019] _Elena Voita, David Talbot, Fedor Moiseev, Rico Sennrich, Ivan Titov_.
   - analysis which head is most effect in MT
   - only a small subset of heads are important for translation.
   - Important Heads have one or more specialized and interpretable functions.
2. [**Attention is not Explanation**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Attention/AttentionNotExplanation.pdf) [NAACL 2019] _Sarthak Jain, Byron C. Wallace_.
   - Attention weighted weakly correction with feature weighted.
   - even same alternative attention can change the prediction.
3. [**A Mixture of h − 1 Heads is Better than h Heads**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Attention/h-1Heads.pdf) [ACL 2020] _Hao Peng, Roy Schwartz, Dianqi Li, Noah A. Smith_.
   - Multi-head attention be seen as an uniform, input-agnostic mixture of experts.
   - introduce MAE which complements the experts with a learned, input-dependent function that assigns their responsibilities.
   - propose a two-step algorithm based on block coordinate descent.
