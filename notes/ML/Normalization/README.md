# Normalization

1. [Rethinking Batch Normalization in Transformers](https://github.com/iofu728/PaperRead/bl/master/paper/ML/Normalization/BNinTransformer.pdf) [-] _Sheng Shen, Zhewei Yao, Amir Gholami, Michael Mahoney, Kurt Keutzer_.
   - BN not work in NLP architecture due to the high variance.
   - proposal an PN architecture (Power Normalization).
     - using quadratic mean instead of variance.
     - approximate backpropagation instead of calculate backpropagation.
