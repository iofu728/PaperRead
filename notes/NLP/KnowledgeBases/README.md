# Knowledge Bases

## Entity -> improve LMs

1. [**K-BERT: Enabling Language Representation with Knowledge Graph**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/K-BERT.pdf) [AAAI 2020 Reject] _Weijie Liu, Peng Zhou, Zhe Zhao, Zhiruo Wang, Qi Ju, Haotang Deng, Ping Wang_.
   - change previous word embedding + TranE => add knowledge to sentence(Like annotations)
   - The change maybe have noisy in semantic. So add one mask.
   - The improvement of performance is little.
2. [**Pretrained Encyclopedia: Weakly Supervised Knowledge-Pretrained Language Model**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/PredictingDSusingDistantSupervisionFromSentiment.pdf) [ICLR 2020] _Wenhan Xiong, Jingfei Du, William Yang Wang, Veselin Stoyanov_.
   - add KB in pretrained process.
   - solve the multi-token entity predict problem.
   - random replace entity to same type entity.
   - verify in zero-shot entity and commonsense QA.
3. [**ERNIE: Enhanced Language Representation with Informative Entities**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/ERNIE.pdf) [ACL 2019] _Zhengyan Zhang, Xu Han, Zhiyuan Liu, Xin Jiang, Maosong Sun, Qun Liu_.
   - TransE as entity embedding.
   - Multi-task.
4. [**Informing Unsupervised Pretraining with External Linguistic Knowledge**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/LIBERT.pdf) [-] _Anne Lauscher, Ivan Vulić, Edoardo Maria Ponti, Anna Korhonen, Goran Glavaš_.
   - feed linguistic constraints (synonyms and direct hypernym-hyponym pairs) to BERT as additional training instances
   - predict lexico-semantic relations from constraint embeddings produced by BERT’s encoder
5. [**SenseBERT: Driving Some Sense into BERT**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/SenseBERT.pdf) [-] _Yoav Levine, Barak Lenz, Or Dagan, Dan Padnos, Or Sharir, Shai Shalev-Shwartz, Amnon Shashua, Yoav Shoham_.
   - predict supersense.
6. [**Knowledge Enhanced Contextual Word Representations**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/KnowBert.pdf) [EMNLP 2019] _Matthew E. Peters, Mark Neumann, Robert L. Logan IV, Roy Schwartz, Vidur Joshi, Sameer Singh, Noah A. Smith_.
   - use entity link task(freeze BERT params when train EL and freeze EL params when train BERT.) L=L_BERT + L_EL4. KnowBERT use entity link task(freeze BERT params when train EL and freeze EL params when train BERT.) L=L_BERT + L_EL
7. [**Integrating Graph Contextualized Knowledge into Pre-trained Language Models**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/BERT-MK.pdf) [-] _Bin He, Di Zhou, Jinghui Xiao, Xin jiang, Qun Liu, Nicholas Jing Yuan, Tong Xu_.
   - uses a similar architecture with ERNIE, which uses GATs instead of TransE.
8. [**KEPLER: A Uniﬁed Model for Knowledge Embedding and Pre-trained Language Representation**](https://github.com//iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/KEPLER.pdf) [-] _Xiaozhi Wang, Tianyu Gao, Zhaocheng Zhu, Zhiyuan Liu, Juanzi Li, Jian Tang_.
   - L_MLM + L_ER
9. [**Entities as Experts: Sparse Memory Access with Entity Supervision**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/EntitiesasExperts.pdf) [-] _Thibault Févry, Livio Baldini Soares, Nicholas FitzGerald, Eunsol Choi, Tom Kwiatkowski_.
   - a little like ERNIE + KNN LM.
   - mention detection layer instead of pretrained a mention detection by using BIO tagger.
   - The first Transformer detection mentions.
   - using detection mention to Entity Memory retrieval(Start + End Representation) top-k entity sum.
   - LN(representation, entity representation)
   - Second Transformer.
   - two MLP: 1. MLM 2. entity link. + Mention detection
   - no-overlapping.
   - Mask strategy followed REALM.
10. [**E-BERT: Efficient-Yet-Effective Entity Embeddings for BERT**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/E-BERT.pdf) [ACL 2020] _Nina Poerner, Ulli Waltinger, Hinrich Schütze_.
    - Inject extra embedding to the PLM space.
      - align the embedding space to BERT embedding space by linear layer.
    - Using Wikipedia2Vec which have word vector space and entity vector space in the same space.
    - by training the MSE loss between word vector space and bert embedding to align.
    - using concatenate/replace strategy to inject the extra embedding like BERTRAM.
    - For entity linking task, propose one MLM and Iterative reﬁnement to improve the performance.
11. [**BERTRAM: Improved Word Embeddings Have Big Impact on Contextualized Model Performance**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/BERTRAM.pdf) [ACL 2020] _Timo Schick, Hinrich Schütze_.
    - Inject in high-quantity embedding for rare words.
    - Three way.
      - SHALLOW
      - concatenate
      - replace.
      - BERT into Attentive Mimicking
12. [**Enhancing Pre-Trained Language Representations with Rich Knowledge for Machine Reading Comprehension**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/KT-BERT.pdf) [ACL 2019] _An Yang, Quan Wang, Jing Liu, Kai Liu, Yajuan Lyu, Hua Wu, Qiaoqiao She, Sujian Li_.
    - Align and inject embedding KBs to LMs.
    - Different with E-BERT, they don't align the embedding, instead of BERT Encoder. So they need more infused architecture.

## Adapter-based

1. [**K-Adapter: Infusing Knowledge into Pre-Trained Models with Adapters**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/K-Adapter.pdf) [-] _Ruize Wang, Duyu Tang, Nan Duan, Zhongyu Wei, Xuanjing Huang, Jianshu ji, Guihong Cao, Daxin Jiang, Ming Zhou_.

   - Motivation:
     - Injection of knowledge into pre-trained models is necessary
       - Large pre-trained models learned to struggle to capture rich knowledge/low ability to generalization.
       - More inclined to learn co-occurrence information rather than low frequency but important knowledge.
       - (Not, fail completely on half of eight reasoning tasks)
     - Multi-task pre-training can cause catastrophic forgetting and is expensive in parameters and parallel.
       - Previous knowledge-based method update model parameters in a multi-task learning manner in which conflict/catastrophic of infusing multiply knowledge.
       - The paper proposal an adapter based method to parallel inject knowledge.
   - Detail:
     - The Adapter contains two FFN and one transformer layer.
     - Not each Transformer has Adapter Layer, in this paper, plugin Adapter in RoBERTa Large 0, 11, 23 layers.
     - So need parameters 3\left[2dm+d+m+3m^2+m^2+8m^2+2m\right]=47M
     - Same skip-connect to align in initialize.
     - Concatenate former adapter layer output and now layer transformer output. (And d is 2d? Can we use equal replace concatenate? Because what followed was a linear layer.)
     - The token final output O_k is the concatenate of transformer output and the last adapter output.
     - If infuse multi-knowledge, the token final output is the concatenate of difference knowledge output Concate(O_1, O_2, …).
     - The paper uses two knowledge Adapter: Factual Adapter and Linguistic Adapter.
     - Factual Adapter use relation classification task in T-RE-rc (filter less than 50 entity pairs). Use pooling to align the entity representation length. train the model for 5 epochs using a batch size of 128.
     - Linguistic Adapter uses predicting dependency parser father index task in Book Corpus using the Standford Parser. train the model for 10 epochs using a batch size of 256.
     - BaseLine:
       1. ERNIE align entities from Wikipedia sentences to fact triples in WikiData and pre-trained the embedding using TransE.
       2. LIBERT adds lexical relation classiﬁcation (LRC) task to inject linguistic constraints.
       3. SenseBERT mask token and predict the mask word and supersense(like POS + fine-grain entity)
       4. KnowBERT use entity link task(freeze BERT params when train EL and freeze EL params when train BERT.) L=L_BERT + L_EL
       5. WKLM replace mask to the same type of entities.
       6. BERT-MK uses a similar architecture with ERNIE, which uses GATs instead of TransE.

## plain text -> improve LMs

1. [**REALM: Retrieval-Augmented Language Model Pre-Training**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/REALM.pdf) [-] _Kelvin Guu, Kenton Lee, Zora Tung, Panupong Pasupat, Ming-Wei Chang_.
   - Motivation:
     1. Enhancing knowledge of language models in a retrieval fashion.
     2. For open-domain QA tasks, the relationship between the retrievers and the reader is completed using the invisible variable approach (ORQA). The authors apply this idea to the pre-training phase.
   - retrieve-then-predict.
   - salient span masking
   - null document
   - trivial retrieval
   - initialization-ICT(Inverse Cloze Task) warm-up
   - Discuss:
     1. It seems like initialization is critical to the performance.
     2. The byproduct is an unsupervised retriever and a passage-level representation.
     3. This way of extracting information from unstructured data seems more reasonable than entity level knowledge infusing. (structured/unstructured?)
     4. Notice that the masking scheme has a big impact on the final result. My understanding is that random masking destroys the semantics of x resulting in poor retrieval learning.
     5. Adapting to new knowledge but also can’t answer this question:
        - “Thatcher” for “\_\_ is the prime minister of United Kingdom.”
2. [**Generalization through Memorization: Nearest Neighbor Language Models**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/KNNLM.pdf) [ICLR 2020] _Urvashi Khandelwal, Omer Levy, Dan Jurafsky, Luke Zettlemoyer, Mike Lewis_.
   - Motivation:
     - Enhancing long-range dependence of language models through explicit storage context encoding patterns and KNN.
   - Detail:
     - Using kNN to improve the generalizability of LMs.
     - Generation prepared (contextual representation c*t=├ (w_1,…w*(t-1) ┤), next token w_t) pair-wise memories cache.
     - No fine-tune the pre-trained LMs parameters.
     - , where d is L2 distance function.
     - $p(y | x)=λp_kNN (y | x)+(1-λ)p_LM (y | x)$
     - Using FAISS to reduce search computation.
     - Discuss:
       1. kNN-LM can be seen as a representation of an enhanced mode of significant co-occurrence with semantic similarity.
       2. The datastore data set needs to have a similar or semantically similar distribution to the test set. (This, of course, is true for all language models.
       3. For time-space complexity, the authors mention in openreview that the generation of datastore takes a similar time to model training. The inference phase drops from the original 500 tokens per second to 60 tokens per second.
       4. Whether this mode of representation can be enhanced significantly in other downstream tasks is still missing.
3. [**BERT-kNN: Adding a kNN Search Component to Pretrained Language Models for Better QA**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/BERT-kNN.pdf) [-] _Nora Kassner, Hinrich Schütze_.
   - model same as kNN-LM, except using IR before kNN.
   - The LAMA result is prefect.
