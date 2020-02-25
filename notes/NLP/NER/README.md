# NER

## Nested NER

1. [**Combining Spans into Entities: A Neural Two-Stage Approach for Recognizing Discontiguous Entitie**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/CombingSpansintoEntities.pdf) [EMNLP 2019] _Bailin Wang, Wei Lu_.
   - Improve Traditional Sequence Label Method CRF -> a Neural Method
   - Two-stage: Segment Extraction + Segment Merging
2. [**Neural Architectures for Nested NER through Linearization**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/LinearizationNestNER.pdf) [ACL 2019] _Jana Strakov´a, Milan Straka, Jan Hajiˇc_.
   - Linear Label -> CONLL-like
   - Sort By Priority
     - More Earlier, More Higher Priority
     - More Longer, More Hi Priority
   - order search
   - trivial heuristic merger algorithm
3. [**A General Framework for Information Extraction using Dynamic Span Graphs**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/DyGIE.pdf) [NAACL 2019] _Yi Luan, Dave Wadden, Luheng He, Amy Shah, Mari Ostendorf, Hannaneh Hajishirzi_.
   - IE Framework + Dynamic Span Graph
   - Multi-granularity Represent
     - Token-level
     - Span-level(The Word Neighbor of targe word)
   - Multi-granularity Propagation
   - Beam Search
   - To Solve The Relation info only be used in the first LSTM-layer before.
   - And Solve Pronouns NER Problem.(6.6% improve)
4. [**Entity,Relation,and Event Extraction with Contextualized Span Representations**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/DyGIE++.pdf) [EMNLP 2019] _David Wadden, Ulme Wennberg, Yi Luan, Hannaneh Hajishirzi_.
   - Using Bert Replace the original representation modules
   - Approve The Origin Dynamic Span Graph Module + Bert Bert
5. [**Nested Named Entity Recognition via Second-best Sequence Learning and Decoding**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/SecondBestCRF.pdf) [-] _Takashi Shibuya, Eduard Hovy_.
   - Recursive Separate CRF
   - Add regular to make the outer entity higher priority than inner entity
   - optime calculate complexity
6. [**Query-Based Named Entity Recognition conference**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/QueryBaseNER.pdf) [-] _Yuxian Meng, Xiaoya Li, Zijun Sun, Jiwei Li_.
   - build a schema which make ner task to a query answered task.
   - the transfer of NER task can use the prior info of NER.
7. [**Multi-Grained Named Entity Recognition**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/MultiGrainedNER.pdf) [-] _Congying Xia, Chenwei Zhang, Tao Yang, Yaliang Li, Nan Du, Xian Wu, Wei Fan, Fenglong Ma, Philip Yu_.
   - two-stage framework
   - detection + classification
   - center search
8. [**Merge and Label: A novel neural network architecture for nested NER**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/MergeAndLabel.pdf) [ACL 2019] _Joseph Fisher, Andreas Vlachos_.
   - Two-stage
     - boundaries, 0-1
       - a complexity neural network
       - static layer + structure layer + update layer
     - classification
9. [**A Unified MRC Framework for Named Entity Recognition**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/MRCNER.pdf) [-] _Xiaoya Li, Jingrong Feng, Yuxian Meng, Qinghong Han, Fei Wu, Jiwei Li_.
   - change ner task to a query answered task(same as Query-based NER).
   - and do nested QA to improve the question answered result.
10. [**A Boundary-aware Neural Model for Nested Named Entity Recognition**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/Boundary-awareNestedNER.pdf) [EMNLP 2019] _Changmeng Zheng, Yi Cai, Jingyun Xu, Ho-fung Leung, Guandong Xu_.
    - Boundary-aware + Classification two task.
    - Boundary use BIO -> so assume only have nested NER or flat NER.
    - Classification use the average hidden of the region representation.
    - evaluation in GENIA.
11. [**Knowledge Guided Named Entity Recognition**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/KnowledgeNER.pdf) [-] _Pratyay Banerjee, Kuntal Kumar Pal, Murthy Devarakonda, Chitta Baral_.
    - short paper.
    - view NER task as MAQA.
    - and add Knowledge.
      - Specially, context = entity types + question + definition + example.
    - Evaluation in biomedical dataset.
12. [**Linguistically Informed Relation Extraction and Neural Architectures for Nested Named Entity Recognition in BioNLP-OST 2019**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/LinguisticallyInformedNestedNER.pdf) [BioNLP 2019] _Pankaj Gupta, Usama Yaseen, Hinrich Schütze_.
    - Recursive NER to deal Nested NER problem.
    - Multitask to auxiliary loss.
    - Rank loss + CRF loss.
    - using KB and Bagging.
    - many hand-crafted features.

## Unlabeled

1. [**Learning A Uniﬁed Named Entity Tagger From Multiple Partially Annotated Corpora For Efﬁcient Adaptation**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/UnifiedNETagger.pdf) [CONLL 2020] _Xiao Huang, Li Dong, Elizabeth Boschee, Nanyun Peng_.
   - combine multi-corpus entity
   - the entity tag set of every corpus is different, so the combine is challenge.
   - O can be every entity
   - maximum the total likelihood of all possible tag sequences consistent with the gold label.
2. [**Semi-Supervised Named Entity Recognition with CRF-VAEs**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/CrfVAEInNER.pdf) [-] _Thomas Effland, Michael Collins_.
   - Semi-supervised
   - Using VAE in NER as the amortized approximation posterior.
   - joint tag-encoding Transformer architecture leads to an ≈1% improvement in F1.
   - resolving unlabeled
   - test in pre-train model

## Cross-Lingual

1. [**Enhanced Meta-Learning for Cross-lingual Named Entity Recognition with Minimal Resources**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/Cross-lingualNER.pdf) [AAAI 2020] _Qianhui Wu, Zijia Lin, Guoxin Wang, Hui Chen, Börje F. Karlsson, Biqing Huang, Chin-Yew Lin_.
   - Motivation: direct transfer can't have a good performance, if we use the most similar k sample to fine-tune the source model.
   - k sample is low-sample learning so use the meta-learning.
   - To find the language-independent features mask entity to predict.
   - average loss reflect the high loss token can't influence loss so add the supplement max loss.
   - low-resource.

## Common NER

1. [**GRN: Gated Relation Network to Enhance Convolutional Neural Network for Named Entity Recognition**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/GRN.pdf) [AAAI 2019] _Hui Chen, Zijia Lin, Guiguang Ding, Jianguang Lou, Yusen Zhang, Borje Karlsson_.
   - Improving Long-term abilities of CNN.
   - Four Layer
     - Embed layer - representation layer
     - CNN - Contextualized Layer
     - Gated - Relation Layer
       - can replace to Direct Fused Layer / ATTention
     - CRF
2. [**TENER: Adapting Transformer Encoder for Name Entity Recognition**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/TENER.pdf) [-] _Hang Yan, Bocao Deng, Xiaonan Li, Xipeng Qiu_.
   - improve Transformer preference in NER Task
   - change Position Encoder -> relative Position Encoder
   - remove scaled in MultiHeadAttention
   - also using character-level information
3. [**ner and pos when nothing is capitalized**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/NER&POS.pdf) [EMNLP 2019] _Stephen Mayhew, Tatiana Tsygankova, Dan Roth_.
   - solve capitalize problem in NER and POS.
   - mix cased and uncased sample in training is better way than Truecase.
4. [**Pretrained Encyclopedia: Weakly Supervised Knowledge-Pretrained Language Model**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/PredictingDSusingDistantSupervisionFromSentiment.pdf) [ICLR 2020] _Wenhan Xiong, Jingfei Du, William Yang Wang, Veselin Stoyanov_.
   - add KB in pretrained process.
   - solve the multi-token entity predict problem.
   - random replace entity to same type entity.
   - verify in zero-shot entity and commonsense QA.
5. [**Zero-Shot Relation Extraction via Reading Comprehension**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/ZeroShotMRC.pdf) [CONLL 2017] _Omer Levy, Minjoon Seo, Eunsol Choi, Luke Zettlemoyer_.
   - View NER as a MRC task which good at zero-shot.
   - I think it due to the representation of entity label which replace the traditional project representation space to one flat.
   - The question temperate which is to determine the performance is writer by human.
   - add negative sample which have no correct answer in sentence from other NER dataset.
