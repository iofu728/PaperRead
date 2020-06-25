# Machine Reading Comprehension

1. [**What does BERT Learn from Multiple-Choice Reading Comprehension Datasets?**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/MRC/Multiple-ChoiceMRC.pdf) [-] _Chenglei Si, Shuohang Wang, Min-Yen Kan, Jing Jiang_.
   - Multiple choice MRC.
   - Un-Readable Data Attack:
     - AddSent2Pas-Shufﬂe
     - AddSent2Opt-Shufﬂe
     - AddAns2Opt-Shufﬂe
   - Un-Answerable Data Attack
     - P-Shufﬂe, Q-Shufﬂe, PQ-Shufﬂe
     - P-Remove, Q-Remove, PQ-Remove
2. [**Latent Retrieval for Weakly Supervised Open Domain Question Answering**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/MRC/ORQA.pdf) [ACL 2019] _Kenton Lee, Ming-Wei Chang, Kristina Toutanova_.
   - Latent Retriever.
   - ICT( Inverse Cloze Task )
3. [**Dense Passage Retrieval for Open-Domain Question Answering**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/MRC/QA_DQR.pdf) [-] _Vladimir Karpukhin, Barlas Oğuz, Sewon Min, Patrick Lewis, Ledell Wu, Sergey Edunov, Danqi Chen, Wen-tau Yih_.
   - A better retriever (lightweight) than Lucene BM25.
   - negative sample strategy? in-batch negative sample.
4. [**Open-Domain Question Answering with Pre-Constructed Question Spaces**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/MRC/Pre-Constructed.pdf) [-] _Jinfeng Xiao, Lidan Wang, Franck Dernoncourt, Trung Bui, Tong Sun, Jiawei Han_.
   - Reader-retriever.
   - Offline query-answer sets.
   - Online retrieve similar query.
   - one classifier to judge agree-not.
5. [**Enhancing Answer Boundary Detection for Multilingual Machine Reading Comprehension**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/MRC/BoundaryDetectionMultiMRC.pdf) [ACL 2020] _Fei Yuan, Linjun Shou, Xuanyu Bai, Ming Gong, Yaobo Liang, Nan Duan, Yan Fu, Daxin Jiang_.
   - mMRC + mixMRC + LAKM
   - mixBERT
     - Data Translating (To careful translation, use "[" and "]" in the answer.)
     - Mix multi lingual query-answer
   - LAKM
     - For query, enumerate all n-gram phrase.
     - filter the phrase candidates and find frequent as knowledge phrases.
     - Mask phrases base on mixMRC
