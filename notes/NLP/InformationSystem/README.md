# Information System

1. [**Learning Robust Models for e-Commerce Product Search**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/InformationSystem/QUARTS.pdf) [ACL 2020] _Thanh V. Nguyen, Nikhil Rao, Karthik Subbian_.
   - Motivation: improve the ability of similarity in query-item recall between two most similar item.
   - Classification + Query Generators.
   - Firstly, pre-trained classiﬁcation and query generation.
   - classification = LSTM + attention + FFN (which have improvement)
   - query generation: seq2seq, encoder is classification, decoder is LSTM + Attention use beam search.
   - using one latent to joint this two part.
   - in online test, improve 12.2%, 5.75% in two countries.
