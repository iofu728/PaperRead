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
  - [Summarization](#summarization)
  - [Adversarial](#adversarial)
  - [Bertology](#bertology)
    - [Bert Distilled](#bert-distilled)
    - [Bert Probe](#bert-probe)
  - [Parallelism](#parallelism)
  - [NLG](#nlg)
  - [Text Style Transfer](#text-style-transfer)
  - [Chinese](#chinese)
- [ML](#ml)
  - [Metric Learning](#metric-learning)
  - [Transformer](#transformer)
  - [Attention](#attention)
  - [Tabular Learning](#tabular-learning)
  - [Unbalance Classify](#unbalance-classify)
  - [Demo](#demo)
- [CV](#cv)
  - [Video Prediction](#video-prediction)
- [License](#license)

## NLP

### [NER](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/NER)

| Read   | Public | Conference       | Title                 | HighLight    | Code               | Other     |
| ------ | ------ | ---------------- | --------------------- | ------------ | ------------------ | --------- |
| 191006 | 190926 | submit ICLR 2020 | [CRF-VAEs][24]        | VAE in NER   | -                  | Unlabeled |
| 191006 | 190925 | CONLL 2020       | [UnifiedNETagger][23] | Multi-Corpus | [NewBioNer][10023] | Unlabeled |

#### Nested NER

| Read   | Public | Conference | Title                              | HighLight           | Code                | Other        |
| ------ | ------ | ---------- | ---------------------------------- | ------------------- | ------------------- | ------------ |
| 190916 | 190910 | EMNLP 2019 | [DyGIE++][6]                       | Bertology           | [dygiepp][10006]    | -            |
| 190919 | 190905 | -          | [Second Best CRF][7]               | Recursive CRF       | [secondbest][10007] | optime cost  |
| 190912 | 190903 | EMNLP 2019 | [Combining Spans into Entities][1] | Neural Net->CRF     | [disco_em19][10001] | Two stage    |
| 190920 | 190824 | -          | [Query-based NER][9]               | ->QA                | -                   | usePriorInfo |
| 190812 | 190804 | ACL 2019   | [Linearization Nest NER][4]        | label -> CONLL-like | -                   | Seq2seq      |
| 190703 | 190630 | ACL 2019   | [Merge and label][18]              | Two-stage           | [mergeLabel][10018] | threshold    |
| 190703 | 190620 | ACL 2019   | [Multi-Grained NER][10]            | Two-stage           | [MGNER][10010]      | centerSearch |
| 190707 | 190405 | NAACL 2019 | [DyGIE][5]                         | Dynamic span graph  | [DyGIE][10005]      | IE Framework |

### Summarization

| Read   | Public | Conference | Title        | HighLight    | Code             | Other          |
| ------ | ------ | ---------- | ------------ | ------------ | ---------------- | -------------- |
| 181212 | 170725 | ICML 2017  | [ConvS2S][2] | CNN semantic | [fairseq][10002] | [notes][20002] |

### Adversarial

| Read   | Public | Conference | Title                               | HighLight       | Code                        | Other         |
| ------ | ------ | ---------- | ----------------------------------- | --------------- | --------------------------- | ------------- |
| 190911 | 190829 | EMNLP 2019 | [Universal Adversarial Triggers][3] | Adversarial-NLP | [universal-triggers][10003] | [blog][30003] |

### [Bertology](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Bertology)

| Read   | Public | Conference       | Title        | HighLight    | Code           | Other |
| ------ | ------ | ---------------- | ------------ | ------------ | -------------- | ----- |
| 190928 | 190926 | submit ICLR 2020 | [ALBert][12] | ReduceParams | -              | -     |
| 190801 | 190508 | -                | [UniLM][21]  | three Mask   | [unilm][10021] | -     |

#### [Bert Distilled](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/BertDistilled)

| Read   | Public | Conference       | Title          | HighLight     | Code | Other |
| ------ | ------ | ---------------- | -------------- | ------------- | ---- | ----- |
| 191002 | 190926 | submit ICLR 2020 | [TinyBert][17] | new tew-stage | -    | -     |

#### [Bert Probe](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Probe)

| Read   | Public | Conference | Title                 | HighLight        | Code | Other |
| ------ | ------ | ---------- | --------------------- | ---------------- | ---- | ----- |
| 191014 | 190515 | ACL 2019   | [Bert Rediscover][37] | probe bert layer | -    | -     |

### [Parallelism](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Parallelism)

| Read   | Public | Conference | Title             | HighLight                        | Code                 | Other |
| ------ | ------ | ---------- | ----------------- | -------------------------------- | -------------------- | ----- |
| 191017 | 191005 | -          | [Megatron-LM][38] | parallelism & little code change | [megatron-LM][10038] | -     |

### [NLG](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/NLG)

| Read   | Public | Conference       | Title              | HighLight                | Code               | Other |
| ------ | ------ | ---------------- | ------------------ | ------------------------ | ------------------ | ----- |
| 191005 | 191001 | submit ICLR 2020 | [BertScore][20]    | auto evaluation use bert | [bertScore][10020] | -     |
| 190926 | 190926 | -                | [CTRL][13]         | controllable generation  | [ctrl][10013]      | -     |
| 191010 | 190812 | -                | [UnLikelihood][27] | unLikelihood             |                    | -     |

### [Text Style Transfer](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/TextStyleTransfer)

| Read   | Public | Conference | Title              | HighLight            | Code                  | Other |
| ------ | ------ | ---------- | ------------------ | -------------------- | --------------------- | ----- |
| 191006 | 190925 | EMNLP 2019 | [CrossProject][25] | Latent Space Project | [CrossProject][10025] | -     |

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

| Read   | Public | Conference       | Title                        | HighLight               | Code                  | Other            |
| ------ | ------ | ---------------- | ---------------------------- | ----------------------- | --------------------- | ---------------- |
| 190929 | 190926 | submit ICLR 2020 | [LayerNorm Transformer][14]  | improve warm-up         | -                     | -                |
| 190716 | 190710 | -                | [Large Memory Layer][31]     | KeyValue search         | [XLM][10031]          | [twitter][30031] |
| 190718 | 190624 | NIPS 2019        | [Tensorized Transformer][33] | decompose + param share | -                     | -                |
| 190908 | 190606 | -                | [Macaron Net][15]            | Strange-Macaron         | -                     | [note][30015]    |
| 190718 | 190519 | ACL 2019         | [Adaptive Att span][34]      | adapting span           | [adaptiveSpan][10034] | -                |
| 190719 | 180710 | ICLR 2019        | [Universal Transformer][35]  | Recurrent + ACT         | [UT][10035]           | [slider][30035]  |

### [Attention](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Attention)

| Read   | Public | Conference | Title                           | HighLight                    | Code                          | Other |
| ------ | ------ | ---------- | ------------------------------- | ---------------------------- | ----------------------------- | ----- |
| 190819 | 190607 | ACL 2019   | [Analysis Multi-Head][16]       | every head role              | [heads][10016]                | -     |
| 190619 | 190226 | NAACL 2019 | [Attention not explanation][30] | weighted correction + robust | [AttentionExplanation][10030] | -     |

### [Tabular Learning](https://github.com/iofu728/PaperRead/blob/master/notes/ML/TabularLearning)

| Read   | Public | Conference       | Title        | HighLight | Code                    | Other         |
| ------ | ------ | ---------------- | ------------ | --------- | ----------------------- | ------------- |
| 191006 | 190926 | submit ICLR 2020 | [TabNet][22] | NN method | [googleResearch][10022] | interpretable |

### [Unbalance Classify](https://github.com/iofu728/PaperRead/blob/master/notes/ML/UnbalanceClassify)

| Read   | Public | Conference | Title                    | HighLight               | Code                    | Other |
| ------ | ------ | ---------- | ------------------------ | ----------------------- | ----------------------- | ----- |
| 191011 | 190116 | ICLR 2019  | [Class-Balance Loss][28] | effective number sample | [googleResearch][10028] | -     |

### [Demo](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Demo)

| Read   | Public | Conference | Title              | HighLight   | Code                  | Other |
| ------ | ------ | ---------- | ------------------ | ----------- | --------------------- | ----- |
| 191011 | 191009 | -          | [Transformers][32] | Unified API | [Transformers][10032] | -     |

## CV

### [Video Prediction](https://github.com/iofu728/PaperRead/blob/master/notes/CV/VideoPrediction)

| Read   | Public | Conference       | Title         | HighLight              | Code | Other |
| ------ | ------ | ---------------- | ------------- | ---------------------- | ---- | ----- |
| 191005 | 190926 | submit ICLR 2020 | [CrevNet][19] | information preserving | -    | -     |

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
[20002]: https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Summarization/ConvS2S.md
[30003]: http://www.ericswallace.com/triggers
[30015]: https://zhuanlan.zhihu.com/p/71747175
[30031]: https://twitter.com/guillaumelample/status/1149646895377076224
[30035]: https://mostafadehghani.com/wp-content/uploads/2018/08/Universal_Transformers.pdf
