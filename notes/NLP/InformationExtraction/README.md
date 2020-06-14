# Information Extraction

## Entity

1. [**Empower Entity Set Expansion via Language Model Probing**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/InformationExtraction/CGExpan.pdf) [ACL 2020] _Yunyi Zhang, Jiaming Shen, Jingbo Shang, Jiawei Han_.
   - Tasks: (Entity Set Expansion)
   - Motivation:
     - Avoid selecting ambiguous patterns that may introduce erroneous entities from other non-target semantic classes.
     - “semantic drift”. As bootstrapping is an iterative process, those erroneous entities added at early iterations may shift the class semantics, leading to inferior expansion quality at later iterations. Previous work using additional user inputs to address this issue, like mutually exclusive classes, and negative example entities.
     - A class name can help us identify unambiguous patterns and eliminate erroneous entities like “Europe” and “New York” if we know the class name is “country”, instead of “state” or “city”.
     - Using the contextual Hearst Pattern representation of pre-trained LM to propose new entities.
     - Three-stage pipeline.
       - class name generation.
       - class name ranking.
       - class-guided entity selection.
