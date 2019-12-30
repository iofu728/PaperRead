> **🤧*Some Paper Read By @gunjianpan***
>
> This is a repository like 'douban' personal home page in AI field.

```console
❱❱❱❱❱❱❱ ❱❱❱❱❱❱ ❱❱❱❱❱ ❱❱❱❱ ❱❱❱❱ ❱❱❱ ❱❱ ❱
```

## Categories

- [Categories](#categories)
- [NLP](#nlp)
  - [NER](#ner)
    - [Nested NER](#nested-ner)
  - [Relation Extraction](#relation-extraction)
  - [Summarization](#summarization)
  - [Adversarial](#adversarial)
  - [Common Sense](#common-sense)
  - [Bertology](#bertology)
  - [Distilled](#distilled)
    - [Bert Distilled](#bert-distilled)
    - [Bert Probe](#bert-probe)
    - [Bert DownStream](#bert-downstream)
  - [Parallelism](#parallelism)
  - [NLG](#nlg)
  - [Text Style Transfer](#text-style-transfer)
  - [Discourse Parsing](#discourse-parsing)
  - [Chinese](#chinese)
- [ML](#ml)
  - [Metric Learning](#metric-learning)
  - [Transformer](#transformer)
    - [Relative position embedding](#relative-position-embedding)
  - [Attention](#attention)
  - [Tabular Learning](#tabular-learning)
  - [Unbalance Classify](#unbalance-classify)
  - [Learning With Noisy Labels](#learning-with-noisy-labels)
  - [Multi-task](#multi-task)
  - [Dropout](#dropout)
  - [Demo](#demo)
- [CV](#cv)
  - [Video Prediction](#video-prediction)
- [License](#license)

## NLP

### [NER](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/NER)

| Read   | Public | Conference | Title                 | HighLight                  | Code               | Other     |
| ------ | ------ | ---------- | --------------------- | -------------------------- | ------------------ | --------- |
| 191220 | 190926 | ICLR 2020  | [WKLM][59]            | add KB in pretrain         | -                  | -         |
| 191113 | 191110 | -          | [TENER][49]           | improve Transformer in NER | -                  | -         |
| 191006 | 190926 | -          | [CRF-VAEs][24]        | VAE in NER                 | -                  | Unlabeled |
| 191006 | 190925 | CONLL 2019 | [UnifiedNETagger][23] | Multi-Corpus               | [NewBioNer][10023] | Unlabeled |
| 191020 | 190712 | AAAI 2019  | [GRN][41]             | +Long-term->CNN            | [GRN][10041]       | -         |
| 191220 | 190327 | EMNLP 2019 | [capitalized][58]     | capitalized in ner and pos | -                  | -         |

#### Nested NER

| Read   | Public | Conference | Title                              | HighLight           | Code                | Other        |
| ------ | ------ | ---------- | ---------------------------------- | ------------------- | ------------------- | ------------ |
| 191101 | 191028 | -          | [MRCNER][44]                       | QA gen + Nested QA  | -                   | -            |
| 190916 | 190910 | EMNLP 2019 | [DyGIE++][6]                       | Bertology           | [dygiepp][10006]    | -            |
| 190919 | 190905 | -          | [Second Best CRF][7]               | Recursive CRF       | [secondbest][10007] | optime cost  |
| 190912 | 190903 | EMNLP 2019 | [Combining Spans into Entities][1] | Neural Net->CRF     | [disco_em19][10001] | Two stage    |
| 190920 | 190824 | -          | [Query-based NER][9]               | ->QA                | -                   | usePriorInfo |
| 190812 | 190804 | ACL 2019   | [Linearization Nest NER][4]        | label -> CONLL-like | -                   | Seq2seq      |
| 190703 | 190630 | ACL 2019   | [Merge and label][18]              | Two-stage           | [mergeLabel][10018] | threshold    |
| 190703 | 190620 | ACL 2019   | [Multi-Grained NER][10]            | Two-stage           | [MGNER][10010]      | centerSearch |
| 190707 | 190405 | NAACL 2019 | [DyGIE][5]                         | Dynamic span graph  | [DyGIE][10005]      | IE Framework |

### [Relation Extraction](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/RelationExtraction)

| Read   | Public | Conference | Title                     | HighLight                        | Code            | Other |
| ------ | ------ | ---------- | ------------------------- | -------------------------------- | --------------- | ----- |
| 191216 | 191128 | AAAI 2020  | [Inducing Relation][55]   | Induing Realtion using cloze     | -               | -     |
| 191128 | 190607 | ACL 2019   | [Matching the Blanks][52] | How to use BERT in relation link | [BERTem][10052] | -     |

### Summarization

| Read   | Public | Conference | Title        | HighLight    | Code             | Other          |
| ------ | ------ | ---------- | ------------ | ------------ | ---------------- | -------------- |
| 181212 | 170725 | ICML 2017  | [ConvS2S][2] | CNN semantic | [fairseq][10002] | [notes][20002] |

### Adversarial

| Read   | Public | Conference | Title                               | HighLight       | Code                        | Other         |
| ------ | ------ | ---------- | ----------------------------------- | --------------- | --------------------------- | ------------- |
| 190911 | 190829 | EMNLP 2019 | [Universal Adversarial Triggers][3] | Adversarial-NLP | [universal-triggers][10003] | [blog][30003] |

### [Common Sense](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/CommonSense)

| Read   | Public | Conference | Title        | HighLight                     | Code            | Other |
| ------ | ------ | ---------- | ------------ | ----------------------------- | --------------- | ----- |
| 191218 | 190904 | EMNLP 2019 | [KagNet][56] | Commonsense via KB + Pretrain | [KagNet][10056] | -     |

### [Bertology](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Bertology)

| Read   | Public | Conference | Title         | HighLight                     | Code           | Other |
| ------ | ------ | ---------- | ------------- | ----------------------------- | -------------- | ----- |
| 191112 | 191029 | -          | [BART][48]    | Auto-Encode + Auto-Regressive | -              | -     |
| 191024 | 191024 | -          | [T5][42]      | Decathlon                     | [T5][10042]    | C4    |
| 191113 | 190926 | ICLR 2020  | [ELECTRA][50] | GAN -> difficult MASK         | -              | -     |
| 190928 | 190926 | ICLR 2020  | [ALBert][12]  | ReduceParams                  | -              | -     |
| 190801 | 190508 | -          | [UniLM][21]   | three Mask                    | [unilm][10021] | -     |

### [Distilled](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Distilled)

| Read   | Public | Conference | Title          | HighLight                    | Code | Other |
| ------ | ------ | ---------- | -------------- | ---------------------------- | ---- | ----- |
| 191228 | 190926 | ICLR 2020  | [DEFINE][61]   | reduce embed size + residual | -    | -     |
| 191002 | 190926 | -          | [TinyBert][17] | new tew-stage                | -    | -     |

#### [Bert Distilled](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/BertDistilled)

| Read   | Public | Conference | Title             | HighLight      | Code                  | Other |
| ------ | ------ | ---------- | ----------------- | -------------- | --------------------- | ----- |
| 191018 | 191002 | NIPS 2019  | [DistillBert][39] | support device | [transformers][10039] | -     |
| 191002 | 190926 | -          | [TinyBert][17]    | new tew-stage  | -                     | -     |

#### [Bert Probe](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Probe)

| Read   | Public | Conference | Title                 | HighLight                   | Code          | Other |
| ------ | ------ | ---------- | --------------------- | --------------------------- | ------------- | ----- |
| 191216 | 190904 | EMNLP 2019 | [LM as KB?][54]       | Bert in Relation Extraction | [LAMA][]10054 | -     |
| 191014 | 190515 | ACL 2019   | [Bert Rediscover][37] | probe bert layer            | -             | -     |

#### Bert DownStream

| Read   | Public | Conference | Title               | HighLight   | Code                           | Other |
| ------ | ------ | ---------- | ------------------- | ----------- | ------------------------------ | ----- |
| 191020 | 190827 | EMNLP 2019 | [Sentence Bert][40] | Bert in STS | [sentence-transformers][10040] | -     |

### [Parallelism](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Parallelism)

| Read   | Public | Conference | Title             | HighLight                        | Code                 | Other         |
| ------ | ------ | ---------- | ----------------- | -------------------------------- | -------------------- | ------------- |
| 191017 | 191005 | -          | [Megatron-LM][38] | parallelism & little code change | [megatron-LM][10038] | [blog][30038] |

### [NLG](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/NLG)

| Read   | Public | Conference | Title              | HighLight                | Code               | Other |
| ------ | ------ | ---------- | ------------------ | ------------------------ | ------------------ | ----- |
| 191005 | 191001 | ICLR 2020  | [BertScore][20]    | auto evaluation use bert | [bertScore][10020] | -     |
| 190926 | 190926 | -          | [CTRL][13]         | controllable generation  | [ctrl][10013]      | -     |
| 191010 | 190812 | -          | [UnLikelihood][27] | unLikelihood             |                    | -     |

### [Text Style Transfer](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/TextStyleTransfer)

| Read   | Public | Conference | Title              | HighLight            | Code                  | Other |
| ------ | ------ | ---------- | ------------------ | -------------------- | --------------------- | ----- |
| 191006 | 190925 | EMNLP 2019 | [CrossProject][25] | Latent Space Project | [CrossProject][10025] | -     |

### [Discourse Parsing](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/DiscourseParsing)

| Read   | Public | Conference | Title                            | HighLight                           | Code | Other |
| ------ | ------ | ---------- | -------------------------------- | ----------------------------------- | ---- | ----- |
| 191111 | 191030 | EMNLP 2019 | [Predict DS using sentiment][46] | using sentiment generate DP dataSet | -    | -     |

### [Chinese](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Chinese)

| Read   | Public | Conference | Title       | HighLight    | Code | Other |
| ------ | ------ | ---------- | ----------- | ------------ | ---- | ----- |
| 191013 | 190906 | -          | [NeZha][36] | chinese bert | -    | -     |

## ML

### [Metric Learning](https://github.com/iofu728/PaperRead/tree/master/notes/ML/MetricLearning)

| Read   | Public | Conference | Title                         | HighLight             | Code                        | Other |
| ------ | ------ | ---------- | ----------------------------- | --------------------- | --------------------------- | ----- |
| 190829 | 190525 | NIPS 2019  | [Constellation Loss][8]       | Multiclass n + Triple | [constellation_loss][10008] | -     |
| 191007 | 170406 | CVPR 2017  | [Quadruplet Loss][26]         | two margin            | -                           | -     |
| 190827 | 160601 | CVPR 2016  | [Multi-class N-pair Loss][29] | multi negative sample | -                           | -     |
| 190827 | 150617 | CVPR 2015  | [Triplet Loss][11]            | Triple                | -                           | -     |

### [Transformer](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Transformer)

| Read   | Public | Conference | Title                            | HighLight               | Code                  | Other            |
| ------ | ------ | ---------- | -------------------------------- | ----------------------- | --------------------- | ---------------- |
| 191229 | 191127 | -          | [SHA-RNN][60]                    | RNN + Att               | [sha-rnn][10060]      | -                |
| 191028 | 191022 | ICLR 2020  | [Depth-adaptive Transformer][43] | depth adaptive          | -                     | -                |
| 190929 | 190926 | -          | [LayerNorm Transformer][14]      | improve warm-up         | -                     | -                |
| 190716 | 190710 | -          | [Large Memory Layer][31]         | KeyValue search         | [XLM][10031]          | [twitter][30031] |
| 190718 | 190624 | NIPS 2019  | [Tensorized Transformer][33]     | decompose + param share | -                     | -                |
| 190908 | 190606 | -          | [Macaron Net][15]                | Strange-Macaron         | -                     | [note][30015]    |
| 190718 | 190519 | ACL 2019   | [Adaptive Att span][34]          | adapting span           | [adaptiveSpan][10034] | -                |
| 191118 | 190228 | NAACL 2019 | [Star Transformer][51]           | FFN -> Star Arch        | [fastNLP][10051]      | -                |
| 190719 | 180710 | ICLR 2019  | [Universal Transformer][35]      | Recurrent + ACT         | [UT][10035]           | [slider][30035]  |

#### Relative position embedding

| Read   | Public | Conference | Title                           | HighLight   | Code | Other              |
| ------ | ------ | ---------- | ------------------------------- | ----------- | ---- | ------------------ |
| 191229 | 180306 | NAACL 2018 | [Self-Att with Relative PE][63] | Relative PE | -    | Transformer Writer |

### [Attention](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Attention)

| Read   | Public | Conference | Title                           | HighLight                    | Code                          | Other |
| ------ | ------ | ---------- | ------------------------------- | ---------------------------- | ----------------------------- | ----- |
| 190819 | 190607 | ACL 2019   | [Analysis Multi-Head][16]       | every head role              | [heads][10016]                | -     |
| 190619 | 190226 | NAACL 2019 | [Attention not explanation][30] | weighted correction + robust | [AttentionExplanation][10030] | -     |

### [Tabular Learning](https://github.com/iofu728/PaperRead/blob/master/notes/ML/TabularLearning)

| Read   | Public | Conference | Title        | HighLight | Code                    | Other         |
| ------ | ------ | ---------- | ------------ | --------- | ----------------------- | ------------- |
| 191006 | 190926 | -          | [TabNet][22] | NN method | [googleResearch][10022] | interpretable |

### [Unbalance Classify](https://github.com/iofu728/PaperRead/blob/master/notes/ML/UnbalanceClassify)

| Read   | Public | Conference | Title                    | HighLight               | Code                    | Other |
| ------ | ------ | ---------- | ------------------------ | ----------------------- | ----------------------- | ----- |
| 191111 | 191107 | -          | [Dice Loss in NLP][47]   | like F1 FP==FN          | -                       | -     |
| 191011 | 190116 | ICLR 2019  | [Class-Balance Loss][28] | effective number sample | [googleResearch][10028] | -     |

### [Learning With Noisy Labels](https://github.com/iofu728/PaperRead/blob/master/notes/ML/LearningWithNoisyLabels)

| Read   | Public | Conference | Title             | HighLight       | Code                 | Other |
| ------ | ------ | ---------- | ----------------- | --------------- | -------------------- | ----- |
| 191029 | 181030 | NIPS 2018  | [Co-teaching][45] | Memorize effect | [Co-teaching][10045] | -     |

### [Multi-task](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Multi-task)

| Read   | Public | Conference | Title                             | HighLight                 | Code         | Other |
| ------ | ------ | ---------- | --------------------------------- | ------------------------- | ------------ | ----- |
| 191216 | 170214 | ECCV 2016  | [Learning without forgetting][53] | Multi-task by no old data | [LwF][10053] | -     |

### [Dropout](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Dropout)

| Read   | Public | Conference | Title        | HighLight        | Code | Other |
| ------ | ------ | ---------- | ------------ | ---------------- | ---- | ----- |
| 191228 | 190926 | ICLR 2020  | [Mixout][62] | origin + dropout | -    | -     |

### [Demo](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Demo)

| Read   | Public | Conference   | Title                   | HighLight            | Code                  | Other |
| ------ | ------ | ------------ | ----------------------- | -------------------- | --------------------- | ----- |
| 191218 | 191015 | [ICMLA 2019] | [ComprehendMedical][57] | Medical NER + RE API | [AWS][10057]          | -     |
| 191011 | 191009 | -            | [Transformers][32]      | Unified API          | [Transformers][10032] | -     |

## CV

### [Video Prediction](https://github.com/iofu728/PaperRead/blob/master/notes/CV/VideoPrediction)

| Read   | Public | Conference | Title         | HighLight              | Code | Other |
| ------ | ------ | ---------- | ------------- | ---------------------- | ---- | ----- |
| 191005 | 190926 | ICLR 2020  | [CrevNet][19] | information preserving | -    | -     |

## License

[Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.en)

Copyright (c) 2019-present, gunjianpan(iofu728)

[1]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/CombingSpansintoEntities.pdf
[2]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Summarization/ConvS2S.pdf
[3]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Adversarial/UniversalAdversarialTriggers.pdf
[4]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/LinearizationNestNER.pdf
[5]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/DyGIE.pdf
[6]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/DyGIE++.pdf
[7]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/SecondBestCRF.pdf
[8]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/ConstellationLoss.pdf
[9]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/QueryBaseNER.pdf
[10]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/MultiGrainedNER.pdf
[11]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/FaceNet.pdf
[12]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/ALBert.pdf
[13]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NLG/ctrl.pdf
[14]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/LayerNormTransformer.pdf
[15]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/MacaronNet.pdf
[16]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Attention/AnalysisMultiHeadAttention.pdf
[17]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/BertDistilled/TinyBert.pdf
[18]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/MergeAndLabel.pdf
[19]: https://github.com/iofu728/PaperRead/blob/master/paper/CV/VideoPrediction/CrevNet.pdf
[20]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NLG/BertScore.pdf
[21]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/UniLM.pdf
[22]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/TabularLearning/TabNet.pdf
[23]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/UnifiedNETagger.pdf
[24]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/CrfVAEInNER.pdf
[25]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/TextStyleTransfer/SemisupervisedTextStyleTransfer.pdf
[26]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/QuadrupletLoss.pdf
[27]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NLG/Unlikelihood.pdf
[28]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/UnbalanceClassify/Class-BalancedLoss.pdf
[29]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/Multi-classN-pairLoss.pdf
[30]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Attention/AttentionNotExplanation.pdf
[31]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/LargeMemoryLayers.pdf
[32]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Demo/Transformers.pdf
[33]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/TensorizedTransformer.pdf
[34]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/AdaptiveAttSpanInTransformer.pdf
[35]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/UniversalTransformers.pdf
[36]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Chinese/NeZha.pdf
[37]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Probe/BertRediscovers.pdf
[38]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Parallelism/MegatronLM.pdf
[39]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/BertDistilled/DistilBERT.pdf
[40]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/SentenceBert.pdf
[41]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/GRN.pdf
[42]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/T5.pdf
[43]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/DepthAdaptiveTransformer.pdf
[44]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/MRCNER.pdf
[45]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/LearningWithNoisyLabels/Co-teaching.pdf
[46]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/DiscourseParsing/PredictingDSusingDistantSupervisionFromSentiment.pdf
[47]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/UnbalanceClassify/DiceLoss.pdf
[48]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/BART.pdf
[49]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/TENER.pdf
[50]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/ELECTRA.pdf
[51]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/StarTransformer.pdf
[52]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/MatchingtheBlanks.pdf
[53]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Multi-task/LearningWithoutForgot.pdf
[54]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Probe/LMasKB.pdf
[55]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/InducingRelationfromBERT.pdf
[56]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/CommonSense/KagNet.pdf
[57]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Demo/ComprehendMedical.pdf
[58]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/NER&POS.pdf
[59]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/PredictingDSusingDistantSupervisionFromSentiment.pdf
[60]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/SHA-RNN.pdf
[61]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Distilled/DEFINE.pdf
[62]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Dropout/Mixout.pdf
[10001]: https://github.com/berlino/disco_em19
[10002]: https://github.com/facebookresearch/fairseq
[10003]: https://github.com/Eric-Wallace/universal-triggers
[10005]: https://github.com/luanyi/DyGIE
[10006]: https://github.com/dwadden/dygiepp
[10007]: https://github.com/yahshibu/nested-ner-2019
[10008]: https://git.code.tecnalia.com/comvis_public/piccolo/constellation_loss/
[10010]: https://github.com/congyingxia/Multi-Grained-NER
[10013]: https://www.github.com/salesforce/ctrl
[10016]: https://github.com/lena-voita/the-story-of-heads
[10018]: https://github.com/fishjh2/merge_label
[10020]: https://github.com/Tiiiger/bert_score
[10021]: https://github.com/microsoft/unilm
[10022]: https://github.com/google-research/google-research/tree/master/tabnet
[10023]: https://github.com/xhuang28/NewBioNer
[10025]: https://tinyurl.com/yyc8zkqg
[10028]: https://github.com/vandit15/Class-balanced-loss-pytorch
[10030]: https://github.com/successar/AttentionExplanation
[10031]: https://github.com/facebookresearch/XLM
[10032]: https://github.com/huggingface/transformers
[10034]: https://github.com/facebookresearch/adaptive-span
[10035]: https://github.com/tensorflow/tensor2tensor/blob/master/tensor2tensor/models/research/universal_transformer.py
[10038]: https://github.com/nvidia/megatron-lm
[10039]: https://github.com/huggingface/transformers
[10040]: https://github.com/UKPLab/sentence-transformers
[10041]: https://github.com/HuiChen24/NER-GRN
[10042]: https://github.com/google-research/text-to-text-transfer-transformer
[10045]: https://github.com/bhanML/Co-teaching
[10051]: https://github.com/fastnlp/fastNLP/blob/master/fastNLP/modules/encoder/star_transformer.py
[10052]: https://github.com/zhpmatrix/BERTem
[10053]: https://github.com/lizhitwo/LearningWithoutForgetting
[10054]: https://github.com/facebookresearch/LAMA
[10056]: https://github.com/INK-USC/KagNet
[10057]: https://aws.amazon.com/cn/comprehend/medical/
[10060]: https://github.com/Smerity/sha-rnn
[20002]: https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Summarization/ConvS2S.md
[30003]: http://www.ericswallace.com/triggers
[30015]: https://zhuanlan.zhihu.com/p/71747175
[30031]: https://twitter.com/guillaumelample/status/1149646895377076224
[30035]: https://mostafadehghani.com/wp-content/uploads/2018/08/Universal_Transformers.pdf
[30038]: https://nv-adlr.github.io/MegatronLM
