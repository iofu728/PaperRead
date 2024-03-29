> **🤧*Some Paper Read By @gunjianpan***
>
> This is a repository like 'douban' personal home page in ML & System field.

```console
❱❱❱❱❱❱❱ ❱❱❱❱❱❱ ❱❱❱❱❱ ❱❱❱❱ ❱❱❱❱ ❱❱❱ ❱❱ ❱
```

## Categories

- [Categories](#categories)
- [NLP](#nlp)
  - [Information Extraction](#information-extraction)
    - [Relation Extraction](#relation-extraction)
    - [NER](#ner)
      - [Nested NER](#nested-ner)
      - [Few-shot/Zero-shot](#few-shotzero-shot)
      - [Medical](#medical)
  - [Cross-Lingual](#cross-lingual)
  - [Graph](#graph)
  - [Knowledge Bases](#knowledge-bases)
  - [Language Models](#language-models)
    - [Piece](#piece)
    - [Bertology](#bertology)
      - [Bert Distilled](#bert-distilled)
      - [PLM Compression](#plm-compression)
      - [Bert Probe](#bert-probe)
      - [Bert DownStream](#bert-downstream)
      - [Multi-modality Bert](#multi-modality-bert)
    - [Representation](#representation)
      - [Document-level Representation](#document-level-representation)
    - [Tune](#tune)
  - [NLG](#nlg)
    - [Summarization](#summarization)
    - [NMT](#nmt)
    - [ChatBot](#chatbot)
  - [QA](#qa)
    - [MRC](#mrc)
    - [Dialogue](#dialogue)
  - [Information System](#information-system)
  - [Other](#other)
    - [Text Style Transfer](#text-style-transfer)
    - [Parsing](#parsing)
    - [Chinese](#chinese)
    - [Attack](#attack)
    - [Common Sense](#common-sense)
- [ML](#ml)
  - [Architecture](#architecture)
    - [Transformer](#transformer)
      - [Relative position embedding](#relative-position-embedding)
    - [Attention](#attention)
    - [Normalization](#normalization)
  - [Strategy](#strategy)
    - [Metric Learning](#metric-learning)
    - [Interpretability](#interpretability)
    - [Multi-task](#multi-task)
    - [Regularization](#regularization)
    - [Optimization](#optimization)
    - [Negative Sample](#negative-sample)
  - [Data](#data)
    - [Unbalance Classify](#unbalance-classify)
    - [Noisy Labels](#noisy-labels)
    - [Extreme Classification](#extreme-classification)
    - [Tabular Learning](#tabular-learning)
  - [Applied Data Scrience](#applied-data-scrience)
    - [Table&Chart](#tablechart)
    - [Demo](#demo)
- [CV](#cv)
  - [Video Prediction](#video-prediction)
- [System](#system)
  - [Distribution](#distribution)
  - [SpeedUp](#speedup)
- [License](#license)

## NLP

### [Information Extraction](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/InformationExtraction)

| Read   | Public | Conference | Title          | HighLight                   | Code             | Other |
| ------ | ------ | ---------- | -------------- | --------------------------- | ---------------- | ----- |
| 200614 | 200429 | ACL 2020   | [CGEXpan][147] | Expand entity set using MLM | [CGExpan][10147] | -     |

#### [Relation Extraction](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/RelationExtraction)

| Read   | Public | Conference | Title                                 | HighLight                        | Code            | Other |
| ------ | ------ | ---------- | ------------------------------------- | -------------------------------- | --------------- | ----- |
| 200612 | 200605 | -          | [Relation of Relation][145]           | RoRs                             | [RoE][10145]    | -     |
| 200116 | 200106 | AAAI 2020  | [Improve EL via latent Embedding][74] | improve the embedding            | -               | -     |
| 191216 | 191128 | AAAI 2020  | [Inducing Relation][55]               | Induing Realtion using cloze     | -               | -     |
| 200108 | 190904 | ACL 2019   | [RE view as Multi-turn MRC][69]       | Multi-turn like RL, MRC          | [MRC][10069]    | -     |
| 200115 | 190721 | NLE 2019   | [25 years IE][73]                     | survey IE in past 25years        | -               | -     |
| 191128 | 190607 | ACL 2019   | [Matching the Blanks][52]             | How to use BERT in relation link | [BERTem][10052] | -     |
| 200909 | 190225 | NAACL 2019 | [RE using explicit context][178]      | second order                     | -               | -     |

#### [NER](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/NER)

| Read   | Public | Conference | Title                   | HighLight                  | Code                | Other |
| ------ | ------ | ---------- | ----------------------- | -------------------------- | ------------------- | ----- |
| 200424 | 200416 | ACL 2020   | [Trigger NER][132]      | Template Trigger           | [TriggerNER][10132] | -     |
| 200331 | 191112 | AAAI 2020  | [Attention in NER][115] | XOR Limitation in BiLSTM   | [cross][10115]      | -     |
| 191113 | 191110 | -          | [TENER][49]             | improve Transformer in NER | -                   | -     |
| 191020 | 190712 | AAAI 2019  | [GRN][41]               | +Long-term->CNN            | [GRN][10041]        | -     |
| 191220 | 190327 | EMNLP 2019 | [capitalized][58]       | capitalized in ner and pos | -                   | -     |
| 200107 | 170613 | CONLL 2017 | [zero-shot MRC][67]     | view NER as MRC            | -                   | -     |

##### Nested NER

| Read   | Public | Conference  | Title                              | HighLight           | Code                       | Other        |
| ------ | ------ | ----------- | ---------------------------------- | ------------------- | -------------------------- | ------------ |
| 200923 | 200710 | ACL 2020    | [Pyramid][179]                     | layer like pyramid  | -                          | -            |
| 200517 | 200514 | ACL 2020    | [NERviaDP][136]                    | leaned N\*N         | [biaffine][10136]          | -            |
| 200513 | 200510 | AAAI 2020   | [Boundary-enhance][135]            | Boundary Info       | -                          | -            |
| 200605 | 200501 | ACL 2020    | [Bipartite Flat-Graph NER][138]    | outmost->inmost     | -                          | -            |
| 200924 | 200429 | ACL 2020    | [Instance-Based NER][181]          | KNN                 | [insurance-ner][10181]     | -            |
| 200606 | 200428 | ACL 2020    | [Translation Discontinuous][139]   | Discontinuous       | [discontinuous-ner][10139] | -            |
| 200427 | 200424 | ACL 2020    | [FLAT][134]                        | Position + Lattice  | -                          | Chinese      |
| 200411 | 200327 | AAAI 2020   | [RBM][123]                         | subEntity           | -                          | BiLSTM base  |
| 200223 | 191120 | EMNLP 2019  | [Boundary-aware][84]               | Boundary + Classify | [boundary][10084]          | -            |
| 200223 | 191120 | BioNLP 2019 | [ost][86]                          | Recursive NER       | [ost][10086]               | -            |
| 200223 | 191110 | -           | [KGNER][85]                        | MAQA + Knowledge    | -                          | -            |
| 191101 | 191028 | ACL 2020    | [MRCNER][44]                       | QA gen + Nested QA  | -                          | -            |
| 190916 | 190910 | EMNLP 2019  | [DyGIE++][6]                       | Bertology           | [dygiepp][10006]           | -            |
| 190919 | 190905 | -           | [Second Best CRF][7]               | Recursive CRF       | [secondbest][10007]        | optime cost  |
| 190912 | 190903 | EMNLP 2019  | [Combining Spans into Entities][1] | Neural Net->CRF     | [disco_em19][10001]        | Two stage    |
| 190920 | 190824 | -           | [Query-based NER][9]               | ->QA                | -                          | usePriorInfo |
| 190812 | 190804 | ACL 2019    | [Linearization Nest NER][4]        | label -> CONLL-like | [nested][10004]            | Seq2seq      |
| 190703 | 190630 | ACL 2019    | [Merge and label][18]              | Two-stage           | [mergeLabel][10018]        | threshold    |
| 190703 | 190620 | ACL 2019    | [Multi-Grained NER][10]            | Two-stage           | [MGNER][10010]             | centerSearch |
| 190707 | 190405 | NAACL 2019  | [DyGIE][5]                         | Dynamic span graph  | [DyGIE][10005]             | IE Framework |

##### Few-shot/Zero-shot

| Read   | Public | Conference | Title                    | HighLight    | Code               | Other     |
| ------ | ------ | ---------- | ------------------------ | ------------ | ------------------ | --------- |
| 200906 | 200824 | -          | [Example-based NER][176] | Span + Top k | -                  | Few-shot  |
| 191006 | 190926 | -          | [CRF-VAEs][24]           | VAE in NER   | -                  | Unlabeled |
| 191006 | 190925 | CONLL 2019 | [UnifiedNETagger][23]    | Multi-Corpus | [NewBioNer][10023] | Unlabeled |

##### Medical

| Read   | Public | Conference | Title                                    | HighLight                | Code                               | Other |
| ------ | ------ | ---------- | ---------------------------------------- | ------------------------ | ---------------------------------- | ----- |
| 200908 | 181213 | ACL 2019   | [Joint NER and Assertion Detection][177] | Multi-task + Conditional | [pytorch-conditional-model][10177] | -     |

### [Cross-Lingual](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/CrossLingual)

| Read   | Public | Conference | Title                             | HighLight                       | Code              | Other |
| ------ | ------ | ---------- | --------------------------------- | ------------------------------- | ----------------- | ----- |
| 200414 | 200410 | -          | [XTREME][124]                     | 40language multi-task benchmark | [xtreme][10124]   | -     |
| 200224 | 191114 | AAAI 2020  | [MetaLearningCrossLingualNER][87] | direct transfer + meta-learning | -                 | -     |
| 200611 | 190904 | EMNLP 2019 | [Unicoder][144]                   | three cross-lingual tasks       | [Unicoder][10144] | -     |

### [Graph](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Graph)

| Read   | Public | Conference | Title        | HighLight           | Code           | Other |
| ------ | ------ | ---------- | ------------ | ------------------- | -------------- | ----- |
| 200716 | 200704 | ICML 2020  | [GCNII][170] | residual + identity | [GCNII][10170] | -     |

### [Knowledge Bases](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/KnowledgeBases)

| Read   | Public | Conference | Title            | HighLight                     | Code                | Other           |
| ------ | ------ | ---------- | ---------------- | ----------------------------- | ------------------- | --------------- |
| 200708 | 200704 | ACL 2020   | [EmbedKGQA][166] | multi-hop, missingLink pred   | [EmbedKGQA][10166]  | -               |
| 200628 | 200502 | -          | [BERT-kNN][154]  | add IR in kNN-LM              | -                   | -               |
| 200628 | 200501 | ACL 2020   | [E-BERT][155]    | inject embedding to PLM       | -                   | -               |
| 200628 | 200429 | ACL 2020   | [BERTRAM][157]   | infer embed for rare words    | [bertram][10157]    | -               |
| 200416 | 200415 | -          | [EAE][126]       | Top-K Memory, like ERNIE      | -                   | -               |
| 200714 | 200406 | ACL 2020   | [R-MeN][168]     | Deep KB Embedding             | [R-MeN][10168]      | -               |
| 200402 | 200210 | -          | [REALM][118]     | retrieve-then-predict         | -                   | [blog][30118]   |
| 200306 | 200210 | -          | [K-Adapter][96]  | Plugin Knowledge              | -                   | -               |
| 200308 | 191113 | -          | [KEPLER][105]    | L_RE + L_MLM                  | [WikiData5M][10105] | -               |
| 200630 | 191031 | EMNLP 2019 | [KnowBERT][160]  | entity linker                 | -                   | -               |
| 200308 | 191003 | -          | [BERT_MK][104]   | GATs                          | -                   | -               |
| 200405 | 190926 | ICLR 2020  | [KNN-LM][120]    | KNN improve LM representation | [knnlm][10120]      | [review][30120] |
| 191220 | 190926 | ICLR 2020  | [WKLM][59]       | add KB in pretrain            | -                   | -               |
| 200112 | 190917 | -          | [K-BERT][70]     | Integrated KG to sentence     | [K-BERT][10070]     | -               |
| 200308 | 190909 | EMNLP 2019 | [KnowBERT][103]  | Alternate learning            | [kb][10103]         | -               |
| 200308 | 190905 | -          | [LIBERT][101]    | lexical                       | -                   | -               |
| 200308 | 190815 | -          | [SenseBERT][102] | supersense                    | [bert-sense][10102] | -               |
| 200629 | 190602 | ACL 2019   | [KT-BERT][158]   | inject & align embedding      | [KTNET][10158]      | -               |
| 200308 | 190517 | ACL 2019   | [ERNIE][100]     | TransE                        | [ERNIE][10100]      | -               |

### [Language Models](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/LM)

| Read   | Public | Conference | Title                         | HighLight                        | Code                 | Other           |
| ------ | ------ | ---------- | ----------------------------- | -------------------------------- | -------------------- | --------------- |
| 200228 | 200213 | AAAI 2020  | [LRLM][91]                    | Span level + latent to align     | [lrlm][10091]        | -               |
| 191017 | 191005 | -          | [Megatron-LM][38]             | parallelism & little code change | [megatron-LM][10038] | [blog][30038]   |
| 200302 | 190215 | -          | [ContextualWordRepresent][93] | word embedding                   | -                    | -               |
| 200403 | 180922 | EMNLP 2018 | [CVT][119]                    | windows+NER train unlabeled data | [cvt][10119]         | -               |
| 200228 | 170502 | -          | [NKLM][90]                    | Knowledge + LM                   | -                    | [review][30090] |

#### Piece

| Read   | Public | Conference | Title       | HighLight    | Code | Other |
| ------ | ------ | ---------- | ----------- | ------------ | ---- | ----- |
| 200314 | 190907 | -          | [BBPE][109] | UTF-8 -> BPE | -    | -     |

#### [Bertology](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Bertology)

| Read   | Public | Conference   | Title           | HighLight                     | Code            | Other           |
| ------ | ------ | ------------ | --------------- | ----------------------------- | --------------- | --------------- |
| 200611 | 200610 | -            | [MCBERT][143]   | Hard ELECTRA(Multi-choice)    | [MCBERT][10143] | -               |
| 200421 | 200420 | -            | [MPNet][131]    | split predict and no-predict  | [MPNet][10131]  | -               |
| 200704 | 200228 | ICML 2020    | [UniLMv2][162]  | Pseudo-Masked                 | [unilm][10021]  | -               |
| 191112 | 191029 | -            | [BART][48]      | Auto-Encode + Auto-Regressive | -               | -               |
| 191024 | 191024 | -            | [T5][42]        | Decathlon                     | [T5][10042]     | C4              |
| 200318 | 190926 | ICLR 2020    | [REFORMER][111] | LSH Mask Attention            | [trax][10111]   | [review][30111] |
| 191113 | 190926 | ICLR 2020    | [ELECTRA][50]   | GAN -> difficult MASK         | -               | -               |
| 190928 | 190926 | ICLR 2020    | [ALBert][12]    | ReduceParams                  | -               | -               |
| 190801 | 190508 | NeurIPS 2019 | [UniLM][21]     | three Mask                    | [unilm][10021]  | -               |

##### [Bert Distilled](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Distilled)

| Read   | Public | Conference   | Title                  | HighLight                    | Code                     | Other           |
| ------ | ------ | ------------ | ---------------------- | ---------------------------- | ------------------------ | --------------- |
| 200706 | 200414 | ACL 2020     | [MobileBERT][163]      | task-agnostic low latency    | [mobile-bert][10163]     | [review][30163] |
| 200409 | 200404 | ACL 2020     | [TinyMBERT][122]       | LL RL CE -> BiLSTM           | -                        | -               |
| 200717 | 200525 | -            | [BERT of Theseus][172] | theseus to teach students    | [BERT-of-Theseus][10172] | -               |
| 191018 | 191002 | NeurIPS 2019 | [DistillBert][39]      | support device               | [transformers][10039]    | -               |
| 191228 | 190926 | ICLR 2020    | [DEFINE][61]           | reduce embed size + residual | -                        | -               |
| 191002 | 190926 | -            | [TinyBert][17]         | new tew-stage                | -                        | -               |

##### [PLM Compression](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Compression)

| Read   | Public | Conference         | Title                                 | HighLight                                 | Code                   | Other         |
| ------ | ------ | ------------------ | ------------------------------------- | ----------------------------------------- | ---------------------- | ------------- |
| 210819 | 171103 | ICLR 2018          | [Code Learning][189]                  | Code-Based                                | [code_learning][10189] | -             |
| 210819 | 180324 | AAAI 2019          | [Binarization][190]                   | AutoEncoder Binarization                  | [lossless][10190]      | -             |
| 210819 | 191002 | EMNLP 2020 finding | [DistilledNonlinearCompression][191]  | Matrix Decompose + KD                     | -                      | -             |
| 210819 | 200801 | ACL 2020           | [Adaptive Compression Embedding][188] | Adpative Code-based Embedding Compression | -                      | -             |
| 210819 | 210119 | AAAI 2021          | [Compressed Attn][192]                | Decoder only have two parallel attention  | -                      | -             |
| 210810 | 201023 | NeurIPS 2020       | [Movement Pruning][187]               | 1-st pruning when fine-tune               | [nn_pruning][10187]    | [blog][20187] |

##### [Bert Probe](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Probe)

| Read   | Public | Conference | Title                          | HighLight                         | Code          | Other |
| ------ | ------ | ---------- | ------------------------------ | --------------------------------- | ------------- | ----- |
| 200708 | 200509 | ACL 2020   | [Intermediate-Task][165]       | which intermediate task good      | -             | -     |
| 200627 | 200623 | ACL 2020   | [Climbing towards NLU][153]    | metaphysical(meaning/linguistic)  | -             | -     |
| 200628 | 200227 | -          | [Primer in BERTology][156]     | What knowledge does BERT have     | -             | -     |
| 191216 | 190904 | EMNLP 2019 | [LM as KB?][54]                | Bert in Relation Extraction       | [LAMA][10054] | -     |
| 200320 | 190624 | ACL 2019   | [RightForTheWrongReasons][113] | bad in some anti-heuristic sample | -             | -     |
| 191014 | 190515 | ACL 2019   | [Bert Rediscover][37]          | probe bert layer                  | -             | -     |

##### Bert DownStream

| Read   | Public | Conference | Title               | HighLight                         | Code                           | Other |
| ------ | ------ | ---------- | ------------------- | --------------------------------- | ------------------------------ | ----- |
| 200113 | 191031 | -          | [DuoBERT][71]       | Three-stage Recall-Rank(pairwise) | [DuoBERT][10071]               | -     |
| 191020 | 190827 | EMNLP 2019 | [Sentence Bert][40] | Bert in STS                       | [sentence-transformers][10040] | -     |

##### Multi-modality Bert

| Read   | Public | Conference | Title                | HighLight                  | Code | Other |
| ------ | ------ | ---------- | -------------------- | -------------------------- | ---- | ----- |
| 200924 | 200917 | -          | [GraphCodeBERT][180] | AST Edge Pred + Node Align | -    | -     |
| 200221 | 200219 | -          | [CodeBERT][82]       | NL + PL                    | -    | -     |

##### [Prompt](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Prompt)

| Read   | Public | Conference | Title                                  | HighLight                  | Code         | Other |
| ------ | ------ | ---------- | -------------------------------------- | -------------------------- | ------------ | ----- |
| 210722 | 210406 | NAACL 2021 | [HowManyDataPointsIsAPromptWorth][185] | head vs prompt in Few-shot | [pet][10185] | -     |

#### [Representation](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Representation)

| Read   | Public | Conference | Title         | HighLight                     | Code            | Other |
| ------ | ------ | ---------- | ------------- | ----------------------------- | --------------- | ----- |
| 210421 | 210420 | -          | [SimCSE][182] | Dropout, Contrastive Learning | [SimCSE][10182] | -     |

##### [Document-level Representation](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/DocumentRepresentation)

| Read   | Public | Conference | Title                    | HighLight                              | Code | Other |
| ------ | ------ | ---------- | ------------------------ | -------------------------------------- | ---- | ----- |
| 200418 | 200415 | ACL 2020   | [Citation-informed][127] | Triplet Loss Negative base on citation | -    | -     |

#### Tune

| Read   | Public | Conference | Title                    | HighLight                  | Code                  | Other |
| ------ | ------ | ---------- | ------------------------ | -------------------------- | --------------------- | ----- |
| 200420 | 200224 | -          | [Self-Distillation][128] | study gold + self-ensemble | -                     | -     |
| 200308 | 190515 | ICML 2019  | [PALs][99]               | Project Att                | [Bert-n-Pals][10099]  | -     |
| 200308 | 190113 | ICML 2019  | [Adapter-BERT][98]       | Fine-tune => Adapter       | [adapter-bert][10098] | -     |

### [NLG](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/NLG)

| Read   | Public | Conference | Title                  | HighLight                                | Code               | Other           |
| ------ | ------ | ---------- | ---------------------- | ---------------------------------------- | ------------------ | --------------- |
| 200303 | 190926 | ICLR 2020  | [Nucleus Sampling][94] | Top-p Sampling                           | [gpt2][10094]      | [review][30094] |
| 200302 | 190926 | ICLR 2020  | [D2GPo][92]            | negative influence <br>-> prior Gaussian | -                  | -               |
| 191005 | 190926 | ICLR 2020  | [BertScore][20]        | auto evaluation use bert                 | [bertScore][10020] | -               |
| 190926 | 190926 | -          | [CTRL][13]             | controllable generation                  | [ctrl][10013]      | -               |
| 191010 | 190812 | -          | [UnLikelihood][27]     | unLikelihood                             |                    | -               |

#### [Summarization](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Summarization)

| Read   | Public | Conference | Title                          | HighLight                                  | Code             | Other             |
| ------ | ------ | ---------- | ------------------------------ | ------------------------------------------ | ---------------- | ----------------- |
| 200313 | 190708 | ACL 2019   | [ExtractiveSummarization][108] | Diff Architecture Extractive Summarization | [fastNLP][10108] | [homepage][30108] |
| 181212 | 170725 | ICML 2017  | [ConvS2S][2]                   | CNN semantic                               | [fairseq][10002] | [notes][20002]    |

#### [NMT](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/NMT)

| Read   | Public | Conference | Title                               | HighLight                         | Code                 | Other |
| ------ | ------ | ---------- | ----------------------------------- | --------------------------------- | -------------------- | ----- |
| 200626 | 200618 | -          | [DeeperEncoder,ShallowDecoder][152] | reduce decoder layer              | -                    | -     |
| 200629 | 191110 | ACL 2020   | [Sandwich][159]                     | improve the FFN & MHA order       | [sandwich][10159]    | -     |
| 200113 | 171107 | ICLR 2018  | [No-autoregressive NMT][72]         | fertilities to auxiliary parallel | [nonauto-nmt][10072] | -     |

#### [ChatBot](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/ChatBot)

| Read   | Public | Conference | Title        | HighLight                     | Code | Other         |
| ------ | ------ | ---------- | ------------ | ----------------------------- | ---- | ------------- |
| 200401 | 200227 | -          | [Meena][117] | Evolved Transformer + Billion | -    | [blog][30117] |

### QA

#### [MRC](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/MRC)

| Read   | Public | Conference | Title                        | HighLight              | Code          | Other |
| ------ | ------ | ---------- | ---------------------------- | ---------------------- | ------------- | ----- |
| 200623 | 200602 | -          | [Pre-Constructed][150]       | reader-retriever       | -             | -     |
| 200623 | 200508 | ACL 2002   | [BoundaryDetectionMRC][151]  | mixMRC + LAKM          | -             | -     |
| 200316 | 191028 | -          | [Multiple-Choice MRC][110]   | Multi-choice + Probing | -             | -     |
| 200609 | 200502 | -          | [DensePassageRetrieval][141] | Dense Retrieval        | [qa-dpr][141] | -     |
| 200405 | 190627 | ACL 2019   | [ORQA][121]                  | Latent Retriever       | -             | -     |

#### [Dialogue](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Dialogue)

| Read   | Public | Conference | Title              | HighLight                   | Code                 | Other |
| ------ | ------ | ---------- | ------------------ | --------------------------- | -------------------- | ----- |
| 200728 | 200505 | ACL 2020   | [ConceptFlow][175] | multi-hop in dialogue       | [ConceptFlow][10175] | -     |
| 200415 | 200409 | ACL 2020   | [MuTual][125]      | Reason Multi-tune Benchmark | [MuTual][10125]      | -     |

### [Information System](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/InformationSystem)

| Read   | Public | Conference | Title         | HighLight                      | Code | Other |
| ------ | ------ | ---------- | ------------- | ------------------------------ | ---- | ----- |
| 200707 | 200507 | ACL 2020   | [QUARTS][164] | Adversarial improve similarity | -    | -     |

### Other

#### [Text Style Transfer](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/TextStyleTransfer)

| Read   | Public | Conference | Title              | HighLight            | Code                  | Other |
| ------ | ------ | ---------- | ------------------ | -------------------- | --------------------- | ----- |
| 191006 | 190925 | EMNLP 2019 | [CrossProject][25] | Latent Space Project | [CrossProject][10025] | -     |

#### [Parsing](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Parsing)

| Read   | Public | Conference | Title                            | HighLight                           | Code                       | Other           |
| ------ | ------ | ---------- | -------------------------------- | ----------------------------------- | -------------------------- | --------------- |
| 200622 | 200610 | ACL 2020   | [Perturbed Masking][149]         | $d(x\\{x_i}, x\\{x_i, x_j})$        | [Perturbed-Masking][10149] | -               |
| 191111 | 191030 | EMNLP 2019 | [Predict DS using sentiment][46] | using sentiment generate DP dataSet | -                          | -               |
| 200421 | 190129 | CONLL 2018 | [Universal DP][129]              | pipeline dp                         | [stanfordnlp][10129]       | -               |
| 200601 | 170310 | ICLR 2017  | [Biaffine][137]                  | graph-based                         | [stanfordnlp][10137]       | [review][30137] |

#### [Chinese](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Chinese)

| Read   | Public | Conference | Title           | HighLight               | Code              | Other |
| ------ | ------ | ---------- | --------------- | ----------------------- | ----------------- | ----- |
| 200714 | 200513 | ACL 2020   | [SpellGCN][169] | phonological + semantic | [SpellGCN][10169] | -     |
| 191013 | 190906 | -          | [NeZha][36]     | chinese bert            | -                 | -     |

#### [Attack](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Attack)

| Read   | Public | Conference | Title                               | HighLight       | Code                        | Other         |
| ------ | ------ | ---------- | ----------------------------------- | --------------- | --------------------------- | ------------- |
| 200717 | 200414 | ACL 2020   | [Weight Poison Attacks][171]        | Weight Poison   | [RIPPLe][10171]             | -             |
| 190911 | 190829 | EMNLP 2019 | [Universal Adversarial Triggers][3] | Adversarial-NLP | [universal-triggers][10003] | [blog][30003] |

#### [Common Sense](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/CommonSense)

| Read   | Public | Conference | Title            | HighLight                     | Code                                  | Other |
| ------ | ------ | ---------- | ---------------- | ----------------------------- | ------------------------------------- | ----- |
| 191218 | 190904 | EMNLP 2019 | [KagNet][56]     | Commonsense via KB + Pretrain | [KagNet][10056]                       | -     |
| 200107 | 190604 | ACL 2019   | [quantities][68] | Rule-base Quantity            | [distribution-over-quantities][10068] | -     |

## ML

### Architecture

#### [Transformer](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Transformer)

| Read   | Public | Conference   | Title                            | HighLight               | Code                  | Other            |
| ------ | ------ | ------------ | -------------------------------- | ----------------------- | --------------------- | ---------------- |
| 200721 | 200712 | ICML 2020    | [T-Fixup][173]                   | param initial=>warm up  | [tfixup][10173]       | -                |
| 200708 | 200707 | ACL 2020     | [Long-range Memory?][167]        | Do need LRM?            | -                     | -                |
| 200426 | 200410 | -            | [Longformer][133]                | Global + slide Win Att  | [longformer][10133]   | -                |
| 191229 | 191127 | -            | [SHA-RNN][60]                    | RNN + Att               | [sha-rnn][10060]      | -                |
| 200608 | 191022 | ICLR 2020    | [LiteTransformer][140]           | Global + Local          | [lite][10140]         | [review][30140]  |
| 191028 | 191022 | ICLR 2020    | [Depth-adaptive Transformer][43] | depth adaptive          | -                     | -                |
| 190929 | 190926 | -            | [LayerNorm Transformer][14]      | improve warm-up         | -                     | -                |
| 190716 | 190710 | -            | [Large Memory Layer][31]         | KeyValue search         | [XLM][10031]          | [twitter][30031] |
| 190718 | 190624 | NeurIPS 2019 | [Tensorized Transformer][33]     | decompose + param share | -                     | -                |
| 190908 | 190606 | -            | [Macaron Net][15]                | Strange-Macaron         | -                     | [note][30015]    |
| 190718 | 190519 | ACL 2019     | [Adaptive Att span][34]          | adapting span           | [adaptiveSpan][10034] | -                |
| 191118 | 190228 | NAACL 2019   | [Star Transformer][51]           | FFN -> Star Arch        | [fastNLP][10051]      | -                |
| 190719 | 180710 | ICLR 2019    | [Universal Transformer][35]      | Recurrent + ACT         | [UT][10035]           | [slider][30035]  |

##### Transformer in CV

| Read   | Public | Conference | Title       | HighLight                    | Code          | Other |
| ------ | ------ | ---------- | ----------- | ---------------------------- | ------------- | ----- |
| 210729 | 210407 | -          | [CaiT][186] | LayerScale + Class Attention | [deit][10186] | -     |

##### Relative position embedding

| Read   | Public | Conference | Title                           | HighLight               | Code                    | Other              |
| ------ | ------ | ---------- | ------------------------------- | ----------------------- | ----------------------- | ------------------ |
| 210424 | 210323 | -          | [RoFormer][183]                 | Complex domain          | [RoFormer][10183]       | [RoPE][30183]      |
| 200702 | 200630 | ICLR 2021  | [TUPE][161]                     | reset + untie           | [TUPE][10161]           | -                  |
| 191229 | 190926 | ICLR 2020  | [Complex Order][65]             | Complex WE + PE         | [complex-order][10065]  | explainable        |
| 190425 | 190306 | ACL 2019   | [Transformer-XL][64]            | Recurrent + Relative PE | [Transformer-XL][10064] | reject once        |
| 191229 | 180306 | NAACL 2018 | [Self-Att with Relative PE][63] | Relative PE             | -                       | Transformer Writer |

#### [Attention](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Attention)

| Read   | Public | Conference | Title                           | HighLight                    | Code                          | Other |
| ------ | ------ | ---------- | ------------------------------- | ---------------------------- | ----------------------------- | ----- |
| 200613 | 200513 | ACL 2020   | [h - 1 heads][146]              | learn heads weightAsexpects  | [MAE][10146]                  | -     |
| 190819 | 190607 | ACL 2019   | [Analysis Multi-Head][16]       | every head role              | [heads][10016]                | -     |
| 190619 | 190226 | NAACL 2019 | [Attention not explanation][30] | weighted correction + robust | [AttentionExplanation][10030] | -     |

#### [Normalization](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Normalization)

| Read   | Public | Conference | Title                    | HighLight           | Code | Other |
| ------ | ------ | ---------- | ------------------------ | ------------------- | ---- | ----- |
| 200319 | 200317 | -          | [BN in Transformer][112] | high var in NLP, PN | -    | -     |

### Strategy

#### [Metric Learning](https://github.com/iofu728/PaperRead/tree/master/notes/ML/MetricLearning)

| Read   | Public | Conference   | Title                         | HighLight             | Code                        | Other |
| ------ | ------ | ------------ | ----------------------------- | --------------------- | --------------------------- | ----- |
| 190829 | 190525 | CVPR 2020    | [Circle Loss][116]            | Unified Npair,Softmax | -                           | -     |
| 190829 | 190525 | NeurIPS 2019 | [Constellation Loss][8]       | Multiclass n + Triple | [constellation_loss][10008] | -     |
| 191007 | 170406 | CVPR 2017    | [Quadruplet Loss][26]         | two margin            | -                           | -     |
| 190827 | 160601 | CVPR 2016    | [Multi-class N-pair Loss][29] | multi negative sample | -                           | -     |
| 190827 | 150617 | CVPR 2015    | [Triplet Loss][11]            | Triple                | -                           | -     |

#### [Interpretability](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Interpretability)

| Read   | Public | Conference | Title                             | HighLight                    | Code | Other         |
| ------ | ------ | ---------- | --------------------------------- | ---------------------------- | ---- | ------------- |
| 200307 | 200208 | -          | [Memorization-Generalization][97] | measure degree of generation | -    | Chiyuan Zhang |

#### [Multi-task](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Multi-task)

| Read   | Public | Conference | Title                              | HighLight                 | Code         | Other |
| ------ | ------ | ---------- | ---------------------------------- | ------------------------- | ------------ | ----- |
| 200610 | 190717 | AAAI 2019  | [SNR][142]                         | Flexible connection       | -            | -     |
| 200330 | 181006 | ECCV 2018  | [Dynamic Task Prioritization][114] | Focal Loss Priori         | -            | -     |
| 191216 | 170214 | ECCV 2016  | [Learning without forgetting][53]  | Multi-task by no old data | [LwF][10053] | -     |

#### [Regularization](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Dropout)

| Read   | Public | Conference | Title        | HighLight         | Code | Other |
| ------ | ------ | ---------- | ------------ | ----------------- | ---- | ----- |
| 200727 | 200220 | ICML 2020  | [Flood][174] | give content loss | -    | -     |
| 191228 | 190926 | ICLR 2020  | [Mixout][62] | origin + dropout  | -    | -     |

#### [Optimization](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Optimization)

| Read   | Public | Conference | Title      | HighLight                  | Code          | Other |
| ------ | ------ | ---------- | ---------- | -------------------------- | ------------- | ----- |
| 200227 | 141222 | ICLR 2015  | [Adam][89] | momentum +squared gradient | [Adam][10089] | -     |

#### [Negative Sample](https://github.com/iofu728/PaperRead/tree/master/notes/ML/NegativeSample)

| Read   | Public | Conference | Title                                     | HighLight                                 | Code               | Other |
| ------ | ------ | ---------- | ----------------------------------------- | ----------------------------------------- | ------------------ | ----- |
| 200621 | 200613 | -          | [BYOL][148]                               | self-supervised (remove negative)         | -                  | -     |
| 200119 | 191211 | -          | [NegativeSampleInVAEs][78]                | using VAEs to solve OOD                   | -                  | -     |
| 200117 | 181216 | ICDE 2019  | [NSCaching][76]                           | dynamical probability sampler replace GAN | [NSCashing][10076] | -     |
| 200117 | 180923 | AAAI 2018  | [Incorporating GAN in Entity Linking][75] | using GAN to generate high quality NS     | -                  | -     |
| 200118 | 180105 | AAAI 2018  | [VSE-ens][77]                             | dynamical sampler to reduce sample time   | [VSE-ens][10077]   | -     |
| 200119 | 140621 | AAAI 2014  | [Translating2Hyperplanes][79]             | solve the multi-label problem             | [Knowledge][10079] | -     |

### Data

#### [Unbalance Classify](https://github.com/iofu728/PaperRead/blob/master/notes/ML/UnbalanceClassify)

| Read   | Public | Conference | Title                    | HighLight               | Code                    | Other |
| ------ | ------ | ---------- | ------------------------ | ----------------------- | ----------------------- | ----- |
| 191111 | 191107 | -          | [Dice Loss in NLP][47]   | like F1 FP==FN          | -                       | -     |
| 191011 | 190116 | ICLR 2019  | [Class-Balance Loss][28] | effective number sample | [googleResearch][10028] | -     |

#### [Noisy Labels](https://github.com/iofu728/PaperRead/blob/master/notes/ML/LearningWithNoisyLabels)

| Read   | Public | Conference   | Title             | HighLight       | Code                 | Other |
| ------ | ------ | ------------ | ----------------- | --------------- | -------------------- | ----- |
| 191029 | 181030 | NeurIPS 2018 | [Co-teaching][45] | Memorize effect | [Co-teaching][10045] | -     |

#### [Extreme Classification](https://github.com/iofu728/PaperRead/blob/master/notes/ML/ExtremeClassification)

| Read   | Public | Conference | Title                    | HighLight            | Code                        | Other |
| ------ | ------ | ---------- | ------------------------ | -------------------- | --------------------------- | ----- |
| 200104 | 190926 | ICLR 2020  | [AdversarialSoftmax][66] | negative sample + DT | [AdversarialSoftMax][10066] | -     |

#### [Tabular Learning](https://github.com/iofu728/PaperRead/blob/master/notes/ML/TabularLearning)

| Read   | Public | Conference | Title        | HighLight | Code                    | Other         |
| ------ | ------ | ---------- | ------------ | --------- | ----------------------- | ------------- |
| 191006 | 190926 | -          | [TabNet][22] | NN method | [googleResearch][10022] | interpretable |

### [Applied Data Scrience](https://github.com/iofu728/PaperRead/blob/master/notes/ML/AppliedDataScience)

| Read   | Public | Conference | Title                         | HighLight                       | Code | Other          |
| ------ | ------ | ---------- | ----------------------------- | ------------------------------- | ---- | -------------- |
| 200101 | 190725 | KDD 2019   | [Job Mobility Prediction][80] | Data Encoder + evaluate for job | -    | [video][30080] |

#### Table&Chart

| Read   | Public | Conference | Title                 | HighLight                                | Code | Other |
| ------ | ------ | ---------- | --------------------- | ---------------------------------------- | ---- | ----- |
| 200311 | 190725 | AAAI 2019  | [Table2Analysis][107] | LM + Beam search to get Table Analysis   | -    | -     |
| 200110 | 190725 | AAAI 2019  | [TableSense][81]      | detect Table Boundaries from spreadsheet | -    | -     |

#### [Demo](https://github.com/iofu728/PaperRead/blob/master/notes/ML/Demo)

| Read   | Public | Conference | Title                   | HighLight            | Code                  | Other             |
| ------ | ------ | ---------- | ----------------------- | -------------------- | --------------------- | ----------------- |
| 200421 | 200316 | -          | [Stanza][130]           | RawText Toolkit      | -                     | [homepage][30130] |
| 191218 | 191015 | ICMLA 2019 | [ComprehendMedical][57] | Medical NER + RE API | [AWS][10057]          | -                 |
| 191011 | 191009 | -          | [Transformers][32]      | Unified API          | [Transformers][10032] | -                 |

## CV

### [Video Prediction](https://github.com/iofu728/PaperRead/blob/master/notes/CV/VideoPrediction)

| Read   | Public | Conference | Title         | HighLight              | Code | Other |
| ------ | ------ | ---------- | ------------- | ---------------------- | ---- | ----- |
| 191005 | 190926 | ICLR 2020  | [CrevNet][19] | information preserving | -    | -     |

## System

### [Distribution](https://github.com/iofu728/PaperRead/blob/master/notes/System/Distribution)

| Read   | Public | Conference      | Title           | HighLight                         | Code               | Other        |
| ------ | ------ | --------------- | --------------- | --------------------------------- | ------------------ | ------------ |
| 200310 | 141101 | USENIX ATX 2014 | [Raft][106]     | Consensus algorithm               | -                  | [web][30106] |
| 200304 | 101101 | SIGOPS 2010     | [VM-FT][95]     | Fault-Tolerant replicating        | -                  | -            |
| 200222 | 040301 | OSDI 2004       | [MapReduce][83] | Map + Reduce For distribution cal | [MapReduce][10083] | -            |
| 200225 | 041020 | SOSP 2003       | [GFS][83]       | distribution file system          | -                  | -            |

### [SpeedUp](https://github.com/iofu728/PaperRead/blob/master/notes/System/SpeedUp)

| Read   | Public | Conference | Title           | HighLight           | Code              | Other |
| ------ | ------ | ---------- | --------------- | ------------------- | ----------------- | ----- |
| 210720 | 210422 | NAACL 2021 | [LightSeq][184] | SpeedUp Transformer | [LightSeq][10184] | -     |

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
[38]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP//MegatronLM.pdf
[39]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/BertDistilled/DistilBERT.pdf
[40]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/SentenceBert.pdf
[41]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/GRN.pdf
[42]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/T5.pdf
[43]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/DepthAdaptiveTransformer.pdf
[44]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/MRCNER.pdf
[45]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/LearningWithNoisyLabels/Co-teaching.pdf
[46]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Parsing/PredictingDSusingDistantSupervisionFromSentiment.pdf
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
[59]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/PredictingDSusingDistantSupervisionFromSentiment.pdf
[60]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/SHA-RNN.pdf
[61]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Distilled/DEFINE.pdf
[62]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Dropout/Mixout.pdf
[63]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/RelativePEAtt.pdf
[64]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/Transformer-XL.pdf
[65]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/encoding_word_order_in_complex_embeddings.pdf
[66]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/ExtremeClassification/extreme_classification_via_adversarial_softmax_approximation.pdf
[67]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/ZeroShotMRC.pdf
[68]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/CommonSense/QuantitativeAttributes.pdf
[69]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/REasMulti-turnQA.pdf
[70]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/K-BERT.pdf
[71]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/DuoBert.pdf
[72]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NMT/NoAutoregressiveNMT.pdf
[73]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/25YearsIE.pdf
[74]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/ImprovingEntityLinkingbyModelingLatentEntityTypeInformation.pdf
[75]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/NegativeSample/IncorporatingGANforNegativeSamplinginKnowledgeRepresentationLearning.pdf
[76]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/NegativeSample/NSCaching.pdf
[77]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/NegativeSample/VSE-ens.pdf
[78]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/NegativeSample/NegativeSamplingInVariationalAutoencoders.pdf
[79]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/NegativeSample/KnowledgeGraphEmbeddingbyTranslatingonHyperplanes.pdf
[80]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/AppliedDataScience/JobMobilityPrediction.pdf
[81]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/AppliedDataScience/TableSense_AAAI19.pdf
[82]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/CodeBERT.pdf
[83]: https://github.com/iofu728/PaperRead/blob/master/paper/System/Distribution/mapreduce.pdf
[84]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/Boundary-awareNestedNER.pdf
[85]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/KnowledgeNER.pdf
[86]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/LinguisticallyInformedNestedNER.pdf
[87]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/Cross-lingualNER.pdf
[88]: https://github.com/iofu728/PaperRead/blob/master/paper/System/Distribution/gfs.pdf
[89]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Optimization/Adam.pdf
[90]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/KnowledgeLM.pdf
[91]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/LatentRelationLM.pdf
[92]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NLG/D2GPo.pdf
[93]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/ContextualWordRepresentations.pdf
[94]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NLG/CuriousCaseNTD.pdf
[95]: https://github.com/iofu728/PaperRead/blob/master/paper/System/Distribution/vm-ft.pdf
[96]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/K-Adapter.pdf
[97]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Interpretabilit/PredictingDSusingDistantSupervisionFromSentiment.pdf
[98]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/AdapterBert.pdf
[99]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/PALs.pdf
[100]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/ERNIE.pdf
[101]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/LIBERT.pdf
[102]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/SenseBERT.pdf
[103]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/KnowBert.pdf
[104]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/BERT-MK.pdf
[105]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/KEPLER.pdf
[106]: https://github.com/iofu728/PaperRead/blob/master/paper/System/Distribution/raft-extended.pdf
[107]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/AppliedDataScience/Table2Analysis_AAAI20.pdf
[108]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Summarization/EffectiveNeuralExtractive.pdf
[109]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/Byte-LevelSubwords.pdf
[110]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/MRC/Multiple-ChoiceMRC.pdf
[111]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/Reformer.pdf
[112]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Normalization/BNinTransformer.pdf
[113]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Probe/RightForTheWrongReasons.pdf
[114]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Multi-task/DynamicTaskPrioritizationForMultiTask.pdf
[115]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/Cross_NER.pdf
[116]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/CircleLoss.pdf
[117]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/ChatBot/Meena.pdf
[118]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/REALM.pdf
[119]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/CVT.pdf
[120]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/KNNLM.pdf
[121]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/MRC/ORQA.pdf
[122]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/BertDistilled/TinyMBERT_Multi_lingual_NER_Distillation.pdf
[123]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/RBM.pdf
[124]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/CrossLingual/XTREME.pdf
[125]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Dialogue/MuTual.pdf
[126]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/EntitiesasExperts.pdf
[127]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/DocumentRepresentation/CitationInformed.pdf
[128]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/LM/Self-EnsembleandSelf-Distillation.pdf
[129]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Parsing/UniversalDependencyParsing.pdf
[130]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Demo/Stanza.pdf
[131]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/MPNet.pdf
[132]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/TriggerNER.pdf
[133]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/Longformer.pdf
[134]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/FLAT.pdf
[135]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/BoundaryEnhancedNested.pdf
[136]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/NERDependencyParsing.pdf
[137]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Parsing/biaffine.pdf
[138]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/BipartiteFlat-GraphNER.pdf
[139]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/Transition-basedBioNER.pdf
[140]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/LiteTransformer.pdf
[141]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/MRC/QA_DQR.pdf
[142]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Multi-task/SNR.pdf
[143]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/MC-BERT.pdf
[144]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/CrossLingual/Unicoder.pdf
[145]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/RelationoftheRelations.pdf
[146]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Attention/h-1Heads.pdf
[147]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/InformationExtraction/CGExpan.pdf
[148]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/NegativeSample/BYOL.pdf
[149]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Parsing/PerturbedMasking.pdf
[150]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/MRC/Pre-Constructed.pdf
[151]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/MRC/BoundaryDetectionMultiMRC.pdf
[152]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NMT/DeepEncoderShallowDecoder.pdf
[153]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Probe/climbing_towards_nlu_on_meaning_form_and_understanding_in_the_age_of_data.pdf
[154]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/BERT-kNN.pdf
[155]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/E-BERT.pdf
[156]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Probe/PrimerinBERTology.pdf
[157]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/BERTRAM.pdf
[158]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/KT-BERT.pdf
[159]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NMT/Sandwich.pdf
[160]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/KnowBert.pdf
[161]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/TUPE.pdf
[162]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/UniLMv2.pdf
[163]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Distilled/MobileBERT.pdf
[164]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/InformationSystem/QUARTS.pdf
[165]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Probe/Intermediate-Task.pdf
[166]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/EmbedKGQA.pdf
[167]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/LongRangeMemoryInTransformer.pdf
[168]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/KnowledgeBases/R-MeN.pdf
[169]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Chinese/SpellGCN.pdf
[170]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Graph/SimpleAndDeepGCN.pdf
[171]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Attack/RIPPLe.pdf
[172]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Distilled/BERTofTheseus.pdf
[173]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Transformer/tfixup.pdf
[174]: https://github.com/iofu728/PaperRead/blob/master/paper/ML/Dropout/flood.pdf
[175]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Dialogue/ConceptFlow.pdf
[176]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/Example-BasedNER.pdf
[177]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/JointEntityExtractionandAssertionDetection.pdf
[178]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/RelationExtraction/RelationExtractionusingExplicitContextConditioning.pdf

[179]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/Jue_[ACL2020]_Pyramid.pdf
[180]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/Daya_[X]_GraphCodeBERT.pdf
[181]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NER/Hiroki_[ACL2020]_Instance-BasedNER.pdf
[182]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Representation/TianyuGao_[X]_SimCSE.pdf
[183]: https://arxiv.org/pdf/2104.09864.pdf
[184]: https://arxiv.org/pdf/2010.13887.pdf
[185]: https://arxiv.org/pdf/2103.08493.pdf
[186]: https://arxiv.org/abs/2103.17239
[187]: https://arxiv.org/abs/2005.07683
[188]: https://aclanthology.org/2020.acl-main.364.pdf
[189]: https://arxiv.org/pdf/1711.01068.pdf
[190]: https://arxiv.org/abs/1803.09065
[191]: https://arxiv.org/pdf/1910.06720.pdf
[192]: https://arxiv.org/pdf/2101.00542.pdf
[10001]: https://github.com/berlino/disco_em19
[10002]: https://github.com/facebookresearch/fairseq
[10003]: https://github.com/Eric-Wallace/universal-triggers
[10004]: https://github.com/ufal/acl2019_nested_ner
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
[10064]: https://github.com/kimiyoung/transformer-xl
[10065]: https://github.com/iclr-complex-order/complex-order
[10066]: https://www.dropbox.com/sh/wn040szm4fulwqy/AADv0LSQ-3BindJ9eAhltoO9a?dl=0
[10068]: https://github.com/google-research-datasets/distribution-over-quantities
[10069]: https://github.com/ShannonAI/mrc-for-flat-nested-ner
[10070]: https://github.com/autoliuweijie/K-BERT
[10071]: https://github.com/castorini/duobert
[10072]: https://github.com/salesforce/nonauto-nmt
[10076]: https://github.com/yzhangee/NSCaching
[10077]: https://github.com/slinzhai/VSE-ens
[10079]: https://github.com/jimmywangheng/knowledge_representation_pytorch
[10083]: https://hadoop.apache.org/docs/r1.2.1/mapred_tutorial.html
[10084]: https://github.com/thecharm/boundary-aware-nested-ner
[10086]: https://github.com/uyaseen/bionlp-ost-2019
[10089]: https://github.com/bigdatagenomics/adam
[10091]: https://github.com/neulab/lrlm
[10094]: https://github.com/minimaxir/gpt-2-simple/issues/51
[10098]: https://github.com/google-research/adapter-bert
[10099]: https://github.com/AsaCooperStickland/Bert-n-Pals
[10100]: https://github.com/thunlp/ERNIE
[10102]: https://github.com/uhh-lt/bert-sense
[10103]: https://github.com/allenai/kb
[10105]: https://deepgraphlearning.github.io/project/wikidata5m
[10108]: https://github.com/fastnlp/fastNLP
[10111]: https://github.com/google/trax/tree/master/trax/models/reformer
[10115]: https://github.com/jacobvsdanniel/cross_ner
[10119]: https://github.com/tensorflow/models/tree/master/research/cvt_text
[10120]: https://github.com/urvashik/knnlm
[10124]: https://github.com/google-research/xtreme
[10125]: https://github.com/Nealcly/MuTual
[10129]: https://github.com/stanfordnlp/stanfordnlp
[10131]: https://github.com/microsoft/MPNet
[10132]: https://github.com/INK-USC/TriggerNER
[10133]: https://github.com/allenai/longformer
[10136]: https://github.com/juntaoy/biaffine-ner
[10137]: https://github.com/yzhangcs/parser
[10139]: https://github.com/daixiangau/acl2020-transition-discontinuous-ner
[10140]: https://github.com/mit-han-lab/lite-transformer
[10141]: https://fburl.com/qa-dpr
[10143]: https://github.com/MC-BERT/MC-BERT
[10144]: https://github.com/microsoft/Unicoder
[10145]: https://github.com/FFTYYY/RoR_relation_extraction
[10146]: https://github.com/Noahs-ARK/MAE
[10147]: https://github.com/yzhan238/CGExpan
[10149]: https://github.com/LividWo/Perturbed-Masking
[10157]: https://github.com/timoschick/bertram
[10158]: https://github.com/PaddlePaddle/Research/tree/master/NLP/ACL2019-KTNET
[10159]: https://github.com/ofirpress/sandwich_transformer
[10161]: https://github.com/guolinke/TUPE
[10163]: https://github.com/google-research/google-research/tree/master/mobilebert
[10166]: https://github.com/malllabiisc/EmbedKGQA
[10168]: https://github.com/daiquocnguyen/R-MeN
[10169]: https://github.com/ACL2020SpellGCN/SpellGCN
[10170]: https://github.com/chennnM/GCNII
[10171]: https://github.com/neulab/RIPPLe
[10172]: https://github.com/JetRunner/BERT-of-Theseus
[10173]: https://github.com/layer6ai-labs/T-Fixup
[10175]: https://github.com/thunlp/ConceptFlow
[10177]: https://github.com/donote/pytorch-conditional-model
[10181]: https://github.com/hiroki13/instance-based-ner
[10182]: https://github.com/princeton-nlp/SimCSE
[10183]: https://github.com/ZhuiyiTechnology/roformer
[10184]: https://github.com/bytedance/lightseq
[10185]: https://github.com/TevenLeScao/pet
[10186]: https://github.com/facebookresearch/deit
[10187]: https://github.com/huggingface/nn_pruning
[10189]: https://github.com/msobroza/compositional_code_learning
[10190]: https://github.com/tca19/near-lossless-binarization
[20002]: https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Summarization/ConvS2S.md
[30003]: http://www.ericswallace.com/triggers
[30015]: https://zhuanlan.zhihu.com/p/71747175
[30031]: https://twitter.com/guillaumelample/status/1149646895377076224
[30035]: https://mostafadehghani.com/wp-content/uploads/2018/08/Universal_Transformers.pdf
[30038]: https://nv-adlr.github.io/MegatronLM
[30080]: https://www.kdd.org/kdd2019/accepted-papers/view/a-hierarchical-career-path-aware-neural-network-for-job-mobility-prediction
[30090]: https://openreview.net/forum?id=BJwFrvOeg
[30094]: https://openreview.net/forum?id=rygGQyrFvH
[30106]: https://raft.github.io/
[30108]: http://pfliu.com/InterpretSum/interpretSum.html
[30111]: https://openreview.net/forum?id=rkgNKkHtvB
[30117]: https://ai.googleblog.com/2020/01/towards-conversational-agent-that-can.html
[30118]: https://joeddav.github.io/blog/2020/03/03/REALM.html
[30120]: https://openreview.net/forum?id=HklBjCEKvH
[30130]: https://stanfordnlp.github.io/stanza/
[30137]: https://openreview.net/forum?id=Hk95PK9le
[30140]: https://openreview.net/forum?id=ByeMPlHKPH
[30163]: https://openreview.net/forum?id=SJxjVaNKwB
[30183]: https://kexue.fm/archives/8265
[20187]: https://medium.com/huggingface/sparse-neural-networks-2-n-gpu-performance-b8bc9ce950fc
