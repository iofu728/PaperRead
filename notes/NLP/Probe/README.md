# Probe Task

1. [**BERT Rediscovers the Classical NLP Pipeline**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Probe/BertRediscovers.pdf) [ACL 2019] _Ian Tenney, Dipanjan Das, Ellie Pavlick_.
   - Scalar Mixing Weights, which layers more important?
   - Cumulative Scoring, how many layer need in that task?
2. [**Language Models as Knowledge Bases?**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Probe/LMasKB.pdf) [EMNLP 2019] _Fabio Petroni, Tim Rocktäschel, Patrick Lewis, Anton Bakhtin, Yuxiang Wu, Alexander H. Miller, Sebastian Riedel_.
   - Bert contain relational knowledge, even if without fine-tune.
   - But the experimental can not verify this. Because of the Google-RE and T-REx are both part of Wikipedia which is the train set of BERT.
   - maybe is co-occurrence patterns.
   - the output of BERT is bigger, the more likely to be correct.
   - by using pearson correlation coefficient, to explain the co-occurrence.
   - ELMO is more like to BERT, even if the train set have no wikipedia.
3. [**Right for the Wrong Reasons: Diagnosing Syntactic Heuristics in Natural Language Inference**](https://github.com/iofu728/PaperRead/bl/master/paper/NLP/Probe/RightForTheWrongReasons.pdf) [ACL 2019] _R. Thomas McCoy, Ellie Pavlick, Tal Linzen_.
   - BERT not good at some anti-heuristics samples, like:
     - lexical overlap
     - subsequence
     - constituent
   - proposal an data set which have many anti-heuristics samples, which called as HANS.
4. [**Climbing towards NLU: On Meaning, Form, and Understanding in the Age of Data**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Probe/climbing_towards_nlu_on_meaning_form_and_understanding_in_the_age_of_data.pdf) [ACL 2020] _Emily M. Bender, Alexander Koller_
   - They say Pre-trained don't have the ability to understand the meaning of language.
   - The ability of understanding language two part: meaning + linguistic form.
   - In my opinion, memory is one part of (need big size, like our daily experiments), and co-occurrence is only to ensure the grammar.
   - For domain-specific, the co-occurrence is very important, especially for the entity phrases.
   - For other hand, memory with the specific-topic maybe more important.
     - Does it can work?
5. [**A Primer in BERTology: What we know about how BERT works**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Probe/PrimerinBERTology.pdf) [-] _Anna Rogers, Olga Kovaleva, Anna Rumshisky_.
   - What knowledge does BERT have?
     - BERT representations are hierarchical rather than linear.
     - BERT embeddings encode information about parts of speech, syntactic chunks and roles.
     - syntactic structure is not directly encoded in self-attention weights, but they can be transformed to reﬂect it.
     - BERT takes subject-predicate agreement into account when performing the cloze task.
     - BERT is better able to detect the presence of NPIs (e.g. ”ever”) and the words that allow their use (e.g. ”whether”) than scope violations.
     - BERT does not “understand” negation and is insensitive to malformed input.
     - BERT’s encoding of syntactic structure does not indicate that it actually relies on that knowledge.
   - Semantic knowledge
     - BERT has some knowledge for semantic roles
     - BERT encodes information about entity types, relations, semantic roles, and proto-roles,
     - BERT struggles with representations of numbers
     - for some relation types, vanilla BERT is competitive with methods relying on knowledge bases
     - BERT cannot reason based on its world knowledge.
   - Localizing linguistic knowledge
     - most selfattention heads do not directly encode any nontrivial linguistic information,
     - Some BERT heads seem to specialize in certain types of syntactic relations.
     - no single head has the complete syntactic tree information.
     - attention weights are weak indicators of subjectverb agreement and reﬂexive anafora.
     - even when attention heads specialize in tracking semantic relations, they do not necessarily contribute to BERT’s performance on relevant tasks.
     - lower layers have the most linear word order information.
     - syntactic information is the most prominent in the middle BERT 3 layers.
     - conﬂicting evidence about syntactic chunks.
     - The ﬁnal layers of BERT are the most taskspeciﬁc.
     - semantics is spread across the entire model
   - Training BERT
     - alternative training objectives
   - Future
     - Benchmarks that require verbal reasoning.
     - Developing methods to “teach” reasoning.
     - Learning what happens at inference time.
