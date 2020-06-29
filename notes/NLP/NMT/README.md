# Neural Machine Translation

1. [**Non-Autoregressive Neural Machine Translation**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NMT/NoAutoregressiveNMT.pdf) [ICLR 2018] _Jiatao Gu, James Bradbury, Caiming Xiong, Victor O.K. Li, Richard Socher_.
   - The auxiliary task is fertilities.
   - But it’s not robust in multi-label, so add KD
   - RL in two-stage.
2. [**Deep Encoder, Shallow Decoder: Reevaluating the Speed-Quality Tradeoff in Machine Translation**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NMT/DeepEncoderShallowDecoder.pdf) [-] _Jungo Kasai, Nikolaos Pappas, Hao Peng, James Cross, Noah A. Smith_.
   - Reduce the decoder layer number to improve the inference efficiency.
3. [**Improving Transformer Models by Reordering their Sublayers**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NMT/Sandwich.pdf) [ACL 2020] _Ofir Press, Noah A. Smith, Omer Levy_.
   - Change FFN & MHA order.
