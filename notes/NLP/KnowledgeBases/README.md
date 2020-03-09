# Knowledge Bases

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

2. [**Parameter-Efﬁcient Transfer Learning for NLP**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/AdapterBert.pdf) [ICML 2019] _Neil Houlsby, Andrei Giurgiu, Stanislaw Jastrzebski, Bruna Morrone, Quentin de Laroussilhe, Andrea Gesmundo, Mona Attariyan, Sylvain Gelly_.

   - Motivation:
     1. Cloud service (Pass)
     2. Without forgetting previous knowledge (compare with continual learning)
     3. For multi-task, injection new knowledge need previous data and recurrent train all previous task.
   - Compare with fine-tuning, want to reduce the parameters and also have great performance.
     1. Every Transformer layer has two Adapter modules. 12 × 2
     2. The pre-trained BERT parameters are frozen. (Attention & FFN except LN)
     3. The Adapter contains two FFN, one non-linear and one skip-connect.
     4. The skip-connect is to ensure that the initial state is consistent with pre-trained.
     5. The adding parameters of one Adapter are 2dm + d + m.
     6. Layer Norm also need to update due to the$\gamma,\beta\ in\  y=\frac{x-\mathrm{E}\left[x\right]}{\sqrt{\mathrm{Var}\left[x\right]+\epsilon}}\ast\gamma+\beta$
     7. Total need 2dm + d + m + 2d parameters.
   - - Linear Layer
   - In GLUE and in additional Classification Tasks
   - Difference parameters V.S. Acc
     - Baseline: 1. Fine-turn Top N transformer layer. 2. Only fine-tune LN parameters.
     - reducing the fine-tune layer makes the accuracy dramatically decrease.
     - The generalization of the adapter for the dim is great.
     - Fine-tune LN isn’t useful.
   - Does every Adapter layers are significant?
     1. The single adapter isn’t useful.
     2. 0-4 barely affect performance.
     3. Lower layers extract lower-level features that are shared among tasks, while the higher layers build features that are unique to different tasks.
     4. The Var of initialization parameters cannot too big.
   - Also, test for 1. Add LN/BN 2. Increase num of layers per adapter. 3. Difference activation func. … But the result is similar.

3. [**BERT and PALs: Projected Attention Layers for Efﬁcient Adaptation in Multi-Task Learning**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/PALs.pdf) [ICML 2019] _Asa Cooper Stickland, Iain Murray_.
   - Projected Attention Layers to take task-specific layer to model.
