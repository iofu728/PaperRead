# Neural Language Generation

1. [CTRL: A C ONDITIONAL T RANSFORMER L ANGUAGE M ODEL FOR C ONTROLLABLE G ENERATION](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NLG/ctrl.pdf) [-] Nitish Shirish Keskar, Bryan McCann, Lav R. Varshney, Caiming Xiong, Richard Socher.
   - controllable generation
   - conditional language model
   - two block
     - multi-head attention with k heads that uses a causal mask to preclude attending tp future tokens + LayerNorm
     - FC + LayerNorm
   - controllable domain
     - style by domain
     - more complex control codes
     - triggering specific tasks
     - zero-shot code-mixing
   - future work
     - more controllable
     - extensions to other areas
     - analysis relationship between LM and train data
     - making the interface between human and LM more explicit and intuitive
2. [BERTScore: Evaluating Text Generation with BERT](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NLG/BertScore.pdf) [submit ICLR 2020] Tianyi Zhang, Varsha Kishore, Felix Wu, Kilian Q. Weinberger, Yoav Artzi.
   - using Bert to automatically evaluating text generation
   - more robust than origin metric
   - capture more semantic info and evaluation more semantic level.
   - test in adversarial data sets.
3. [Neural Text Generation with Unlikelihood Training](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/NLG/Unlikelihood.pdf) [-] Sean Welleck, Ilia Kulikov, Stephen Roller, Emily Dinan, Kyunghyun Cho, Jason Weston.
   - some problem in NLG
     - repetition
     - next-token
     - token distribution mismatch
   - Decoder Method
     - Deterministic Decoder
       - greedy search
       - beam search
     - Stochastic Decoder
   - Unlikelihood -> repetition unlikely
     - Token-level
     - sequence-level
   - $$\mathcal{L}_{\mathrm{UL}}^{t}\left(p_{\theta}\left(\cdot | x_{<t}\right), \mathcal{C}^{t}\right)=-\sum_{c \in \mathcal{C}^{t}} \log \left(1-p_{\theta}\left(c | x_{<t}\right)\right)$$
