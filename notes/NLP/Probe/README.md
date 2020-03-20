# Probe Task

1. [**BERT Rediscovers the Classical NLP Pipeline**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Probe/BertRediscovers.pdf) [ACL 2019] _Ian Tenney, Dipanjan Das, Ellie Pavlick_.
   - Scalar Mixing Weights, which layers more important?
   - Cumulative Scoring, how many layer need in that task?
2. [**Language Models as Knowledge Bases?**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Probe/LMasKB.pdf) [EMNLP 2019] _Fabio Petroni, Tim Rocktäschel, Patrick Lewis, Anton Bakhtin, Yuxiang Wu, Alexander H. Miller, Sebastian Riedel_.
   - Bert contain relational knowledge, even if without fine-tune.
   - But the experimental can not verify this. Because of the Google-RE and T-REx are both part of Wikipedia which is the train set of BERT.
   - maybe is co-occurrence patterns.
   - the output of BERT is bigger, the more likely to be correct.
   - by using pearson correlation coefficient, to explain the co-occurrence.
   - ELMO is more like to BERT, even if the train set have no wikipedia.
3. [**Right for the Wrong Reasons: Diagnosing Syntactic Heuristics in Natural Language Inference**](https://github.com/iofu728/PaperRead/bl/master/paper/NLP/Probe/RightForTheWrongReasons.pdf) [ACL 2019] _R. Thomas McCoy, Ellie Pavlick, Tal Linzen_.
   - BERT not good at some anti-heuristics samples, like:
     - lexical overlap
     - subsequence
     - constituent
   - proposal an data set which have many anti-heuristics samples, which called as HANS.
