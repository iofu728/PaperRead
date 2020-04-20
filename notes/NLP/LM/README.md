# Language Models

## Knowledge Language Models

1. [**A Neural Knowledge Language Model**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/KnowledgeLM.pdf) [-] _Sungjin Ahn, Heeyoul Choi, Tanel Pärnamaa, Yoshua Bengio_.
   - add knowledge to Language Models.
   - Tuple(head entity, relation, tail entity).
   - token-level topic knowledge.
   - aligned knowledge.
2. [**Latent Relation Language Models**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/LatentRelationLM.pdf) [AAAI 2020] _Hiroaki Hayashi*, Zecong Hu*, Chenyan Xiong, Graham Neubig_.
   - Span-level.
   - Aligned entity to raw text by latent parameters.
     - span variable
     - source variable
     - relation variable

## Contextual Word Representation

1. [**Contextual Word Representations: A Contextual Introduction**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/ContextualWordRepresentations.pdf) [-] _Noah A. Smith_.
   - Survey of Contextual Word Representations

## Parallelism

1. [**Megatron-LM: Training Multi-Billion Parameter Language Models Using GPU Model Parallelism**](https://github.com/iofu728/PaperRead/blob/master/NLP/Parallelism/Megatron-LM.pdf) [-] _Mohammad Shoeybi, Mostofa Patwary Raul Puri, Patrick LeGresley, Jared Casper, Bryan Catanzaro_.
   - parallelism bert.
   - using Pre-LN Transformer instead of Post-LN Transformer in Origin Bert
   - using the GELU instead of RELU
   - little of code change in parallelism architecture.

## Piece

1. [**Neural Machine Translation with Byte-Level Subwords**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/Byte-LevelSubwords.pdf) [-] _Changhan Wang, Kyunghyun Cho, Jiatao Gu_.
   - UTF-8 -> BPE

## Semi-Supervised

1. [**Semi-Supervised Sequence Modeling with Cross-View Training**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/CVT.pdf) [EMNLP 2018] _Kevin Clark, Minh-Thang Luong, Christopher D. Manning, Quoc V. Le_.
   - Using windows + NER + suoervised model to train the unlabel data.
   - Multi-task.

## Tune

1. [**Parameter-Efﬁcient Transfer Learning for NLP**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/AdapterBert.pdf) [ICML 2019] _Neil Houlsby, Andrei Giurgiu, Stanislaw Jastrzebski, Bruna Morrone, Quentin de Laroussilhe, Andrea Gesmundo, Mona Attariyan, Sylvain Gelly_.

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

2. [**BERT and PALs: Projected Attention Layers for Efﬁcient Adaptation in Multi-Task Learning**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/PALs.pdf) [ICML 2019] _Asa Cooper Stickland, Iain Murray_.
   - Projected Attention Layers to take task-specific layer to model.
3. [**Improving BERT Fine-Tuning via Self-Ensemble and Self-Distillation**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/Self-EnsembleandSelf-Distillation.pdf) [-] _Yige Xu, Xipeng Qiu, Ligao Zhou, Xuanjing Huang_.
   - want to use others method to replace fine-tune.
   - self-ensemble: average the ensemble models.
   - self-distillation: study gold + self-ensemble.
