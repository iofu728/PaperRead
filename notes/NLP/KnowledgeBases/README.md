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

## Adapter-based

1. [**K-Adapter: Infusing Knowledge into Pre-Trained Models with Adapters**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/K-Adapter.pdf) [-] _Ruize Wang, Duyu Tang, Nan Duan, Zhongyu Wei, Xuanjing Huang, Jianshu ji, Guihong Cao, Daxin Jiang, Ming Zhou_.
   - Add some Dense between Transformer block in the Bert-like Architectures to Fine-tune in the downstream task.
   - Bert params freeze.
   - can parallelism.
   - Continue learning.
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
