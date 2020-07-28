# Dialogue

1. [**MuTual: A Dataset for Multi-Turn Dialogue Reasoning**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Dialogue/MuTual.pdf) [ACL 2020] _Leyang Cui, Yu Wu, Shujie Liu, Yue Zhang, Ming Zhou_.
   1. one benchmark of multi-turn dialogue reason to improve the repsonse logical.
   2. base on the Chinese high school English listening comprehension test data.
   3. randomly drop incorrect options util three candidates are left.
   4. change images to text using OCR (dual correct).
   5. negative response are logically correct if the context is not considered, so focus on multi-turn conversation reasoning.
   6. lexical overlap between response and context (9.98)10.63
   7. Human who pass the TEM-8 check.
   8. 6 reason types.
   9. MuTual+ -> randomly replace to safe answers.
2. [**Grounded Conversation Generation as Guided Traverses in Commonsense Knowledge Graphs**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Dialogue/ConceptFlow.pdf) [ACL 2020] _Houyu Zhang, Zhenghao Liu, Chenyan Xiong, Zhiyuan Liu_.
   - Using multi-hop knowledge graph to improve the dialogue.
   - But in fact, the correct response is part of question which depend on person's mind.
   - The base model is a seq2seq generation model which outputs depend on the previous output.
   - First of all, the use one GRU to embedding the word-level information which to gather sequence information.
   - The concept graph(central graph and the outer graph) are based on entity linking systems.
   - the zero-hop information and one-hop information are belong to the central graph.
   - And two-hop information is in the outer graph.
   - They use GraftNet to encoder the graph information which use one FFN and pagerank score to calculate the similarity between each nodes.
   - The outer graph is hopping from start node to the two-hop node by attention mechanism directly.
   - The finial hidden output is concatenate two level attention output to a FFN layer.
     - The text-base representation is a self-attention which base on text sequence.
     - The concept-based representation is concatenate central and outer information.
   - And using one FFN to decision which part of embedding the model will use(like a gater).
   - The experiments compare with two finetune model which base on GPT-2. And this model reduce 70% parameters that GPT-2.
