> 🤧Some paper read by gunjianpan

```console
❱❱❱❱❱❱❱ ❱❱❱❱❱❱ ❱❱❱❱❱ ❱❱❱❱ ❱❱❱❱ ❱❱❱ ❱❱ ❱
```

## NLP

### [NER](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/NER)

| Read   | Public | Conference | Title                              | HighLight           | Code                | Other        |
| ------ | ------ | ---------- | ---------------------------------- | ------------------- | ------------------- | ------------ |
| 190916 | 190910 | EMNLP 2019 | [DyGIE++][6]                       | Bertology           | [dygiepp][10006]    | -            |
| 190919 | 190905 | -          | [Second Best CRF][7]               | Recursive CRF       | [secondbest][10007] | optime cost  |
| 190912 | 190903 | EMNLP 2019 | [Combining Spans into Entities][1] | Neural Net->CRF     | [disco_em19][10001] | Two stage    |
| 190920 | 190824 | -          | [Query-based NER][9]               | ->QA                | -                   | usePriorInfo |
| 190812 | 190804 | ACL 2019   | [Linearization Nest NER][4]        | label -> CONLL-like | -                   | Seq2seq      |
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

| Read   | Public | Conference       | Title        | HighLight    | Code | Other |
| ------ | ------ | ---------------- | ------------ | ------------ | ---- | ----- |
| 190928 | 190926 | submit ICLR 2020 | [ALBert][12] | ReduceParams | -    | -     |

### [Transformer](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Transformer)

| Read   | Public | Conference       | Title                       | HighLight       | Code | Other |
| ------ | ------ | ---------------- | --------------------------- | --------------- | ---- | ----- |
| 190929 | 190926 | submit ICLR 2020 | [LayerNorm Transformer][14] | improve warm-up |      | -     |

### [NLG](https://github.com/iofu728/PaperRead/blob/master/notes/NLP/NLG)

| Read   | Public | Conference | Title      | HighLight               | Code          | Other |
| ------ | ------ | ---------- | ---------- | ----------------------- | ------------- | ----- |
| 190926 | 190926 | -          | [CTRL][13] | controllable generation | [ctrl][10013] | -     |

## ML

### [Metric Learning](https://github.com/iofu728/PaperRead/tree/master/notes/ML/MetricLearning)

| Read   | Public | Conference | Title                   | HighLight             | Code                        | Other |
| ------ | ------ | ---------- | ----------------------- | --------------------- | --------------------------- | ----- |
| 190829 | 190525 | NIPS 2019  | [Constellation Loss][8] | Multiclass n + Triple | [constellation_loss][10008] | -     |
| 190827 | 150617 | CVPR 2015  | [Triplet Loss][11]      | Triple                |                             | -     |

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
[14]: https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Transformer/LayerNormTransformer.pdf
[10001]: https://github.com/berlino/disco_em19
[10002]: https://github.com/facebookresearch/fairseq
[10003]: https://github.com/Eric-Wallace/universal-triggers
[10005]: https://github.com/luanyi/DyGIE
[10006]: https://github.com/dwadden/dygiepp
[10007]: https://github.com/yahshibu/nested-ner-2019
[10008]: https://git.code.tecnalia.com/comvis_public/piccolo/constellation_loss/
[10010]: https://github.com/congyingxia/Multi-Grained-NER
[10013]: https://www.github.com/salesforce/ctrl
[20002]: https://github.com/iofu728/PaperRead/blob/master/notes/NLP/Summarization/ConvS2S.md
[30003]: http://www.ericswallace.com/triggers
