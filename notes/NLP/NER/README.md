# NER

## Nested NER

1. [Combining Spans into Entities: A Neural Two-Stage Approach for Recognizing Discontiguous Entitie](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/CombingSpansintoEntities.pdf) [EMNLP 2019] Bailin Wang, Wei Lu.
   - Improve Traditional Sequence Label Method CRF -> a Neural Method
   - Two-stage: Segment Extraction + Segment Merging
2. [Neural Architectures for Nested NER through Linearization](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/LinearizationNestNER.pdf) [ACL 2019] Jana Strakov´a, Milan Straka, Jan Hajiˇc
   - Linear Label -> CONLL-like
   - Sort By Priority
     - More Earlier, More Higher Priority
     - More Longer, More Hi Priority
   - order search
   - trivial heuristic merger algorithm
3. [A General Framework for Information Extraction using Dynamic Span Graphs](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/DyGIE.pdf) [NAACL 2019] Yi Luan, Dave Wadden, Luheng He, Amy Shah, Mari Ostendorf, Hannaneh Hajishirzi.
   - IE Framework + Dynamic Span Graph
   - Multi-granularity Represent
     - Token-level
     - Span-level(The Word Neighbor of targe word)
   - Multi-granularity Propagation
   - Beam Search
   - To Solve The Relation info only be used in the first LSTM-layer before.
   - And Solve Pronouns NER Problem.(6.6% improve)
4. [Entity,Relation,and Event Extraction with Contextualized Span Representations](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/DyGIE++.pdf) [EMNLP 2019] David Wadden, Ulme Wennberg, Yi Luan, Hannaneh Hajishirzi.
   - Using Bert Replace the original representation modules
   - Approve The Origin Dynamic Span Graph Module + Bert Bert
5. [Nested Named Entity Recognition via Second-best Sequence Learning and Decoding](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/SecondBestCRF.pdf) [-] Takashi Shibuya, Eduard Hovy.
   - Recursive Separate CRF
   - Add regular to make the outer entity higher priority than inner entity
   - optime calculate complexity
6. [Query-Based Named Entity Recognition conference](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/QueryBaseNER.pdf) [-] Yuxian Meng, Xiaoya Li, Zijun Sun, Jiwei Li.
   - build a schema which make ner task to a query answered task.
   - the transfer of NER task can use the prior info of NER.
7. [Multi-Grained Named Entity Recognition](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/MultiGrainedNER.pdf) [-] Congying Xia, Chenwei Zhang, Tao Yang, Yaliang Li, Nan Du, Xian Wu, Wei Fan, Fenglong Ma, Philip Yu.
   - two-stage framework
   - detection + classification
   - center search
8. [Merge and Label: A novel neural network architecture for nested NER](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/MergeAndLabel.pdf) [ACL 2019] Joseph Fisher, Andreas Vlachos.
   - Two-stage
     - boundaries, 0-1
       - a complexity neural network
       - static layer + structure layer + update layer
     - classification

## Unlabeled

1. [Learning A Uniﬁed Named Entity Tagger From Multiple Partially Annotated Corpora For Efﬁcient Adaptation](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/UnifiedNETagger.pdf) [CONLL 2020] Xiao Huang, Li Dong, Elizabeth Boschee, Nanyun Peng.
   - combine multi-corpus entity
   - the entity tag set of every corpus is different, so the combine is challenge.
   - O can be every entity
   - maximum the total likelihood of all possible tag sequences consistent with the gold label.
