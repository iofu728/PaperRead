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
