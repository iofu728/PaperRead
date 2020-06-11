# Bertology

1. [**ALBERT: A L ITE BERT FOR S ELF - SUPERVISED L EARNING OF L ANGUAGE R EPRESENTATIONS**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/ALBert.pdf)[ICLR 2020] _Zhenzhong Lan, Mingda Chen, Sebastian Goodman, Kevin Gimpel, Piyush Sharma, Radu Soricut_.

   - 感觉下来 ALBert 更像是一篇调参实验报告 🍋
   - 整个工作的 Motivation 是减少参数量，加速训练时间，所以 performance 掉一点问题不大
   - 除了三点最大的改进 HighLight
     - 减小 Embedding size，使其不再与 Transformer 的 Hidden Size 相等
     - 共享 Transformer 和 FFN 的参数（这不是在开 Multi-head 的倒车吗
     - 改变 NSP negative sample 的构造方法
   - 还 follow 了一些之前 Bertology 模型的 tricks
     - spanBert 的 n-gram masking
     - 之前 76min 训练 Bert 那篇用到的 LAMB 优化器
   - 对于减小 embed size 这一点，其实在平时实验过程中也深有感触，在有些 Task 上那 bert 的 Embedding 层出来接其他 model，效果可能还会比 Glove 差。尤其是当用 bert-large 的时候，那 embed size 可是有 1024。主要还是 size 太大，太过稀疏，而减小了主要的 feature 维度的贡献。
   - 共享参数大概单纯只是想减小参数维度吧，毕竟 multi-head 的有效性还是摆在那里的。
   - 至于第三点，大概也是随机选择 negative sample 的一个通病吧。在这里给出的解释是之前 random negative sample 容易让模型学习到主题匹配这个比较简单的任务去，而忽略更深层的语义连贯性。
   - 至于模型参数量降下来之后呢，当然是继续增加模型参数啦（ 狗头
   - 至于 bert-xlarge 不 work， 而 ALBert-xlarge work，我的感觉是首先 Embed 层维度被放大太多了，导致信息过于向与上下文偏移吧. 而增加 Hidden size 会使得靠后的 layer 信息进一步被放大. 而 ALBer-xlarge 首先减小 Embed 维度过大的影响, 然后 share 了所有层的参数, 相当于把原来所有 layer 做了个平均(而不是只取最后一层 hidden layer 的输出. 这样实际上会削弱过于像更高层语义信息偏移的趋势. 感觉如果作者做了 ALBert-xlarge 的 no-share 实验应该会有所体现.
   - 而 ALBert-xxlarge 比 ALBert-xlarge 更 work, 感觉也是差不多的原因. 增加 Hidden size 是扩充靠后层级获得的 semantic 信息. 主要是因为做了参数共享,实际上作用到输出的是 layer 的某种平均. ALBert-xlarge 比 ALbert-large work, ALBert-xxlarge 比 ALbert-xlarge work 说明对 ALBert 这种 Language Model 所蕴含的信息量还能通过放大 hidden size 扩充.( 还是觉得少了一组 12 layer 2048 hidden size 的实验, 现在这种情况只能盲猜
   - 总的来说，这是一篇 Betrology 集大成的 paper，文章逻辑实验都写的不错，包括一些 idea 的提出，参考文献的选择，还是建议一看，能加深对 Bertology 的理解。（话说 refer 里面还有 10 多篇没看过 要去面壁了

2. [**Unified Language Model Pre-training for Natural Language Understanding and Generation**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/UniLM.pdf) [-] _Li Dong, Nan Yang, Wenhui Wang, Furu Wei, Xiaodong Liu, Yu Wang, Jianfeng Gao, Ming Zhou, Hsiao-Wuen Hon_.
   - three mask
     - unidirectional
     - bidirectional
     - seq2seq
   - framework support both NLU & NLG
3. [**Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/T5.pdf) [-] _Colin Raffel, Noam Shazeer, Adam Roberts, Katherine Lee, Sharan Narang, Michael Matena, Yanqi Zhou, Wei Li, Peter J. Liu._
   - Natural Language Decathlon.
   - every task -> seq2seq.
     - (TaskName: Sentences) -> (Task result)
     - except regression task -> (1, 1.2, 1.4 ... 5) multi-class classification
   - C4 Colossal Clean Crawled Corpus. by some heuristic method.
   - using teacher forcing + cross-entropy loss.
   - AdaFactor Optimizer + greedy decoding.
   - pack multi seq -> each entity of one batch.
   - inverse square root warm-up strategy $1/sqrt(max(n, k))$
   - SentencePrice -> 32000 vocab
   - like UnifiedLM Architectures -> Prefix LM
   - Test for multi corruption rate & corrupted span lens.
4. [**BART: Denoising Sequence-to-Sequence Pre-training for Natural Language Generation, Translation, and Comprehension**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/BART.pdf) [-] _Mike Lewis, Yinhan Liu, Naman Goyal, Marjan Ghazvininejad, Abdelrahman Mohamed, Omer Levy, Ves Stoyanov, Luke Zettlemoyer_.
   - Auto-ENcode + Auto-Regressive
   - add more noisy to text
   - first, corrupting text with an arbitrary noising function.
   - second, reconstruct the original text.
   - Token Mask + Token Deletion + Text Infilling + Sentence Permutation + Document Rotation
   - LM + Permutation LM + MLM + Multitask MLM + Masked Seq-seq
   - good at NLG
5. [**ELECTRA: Pre-training Text Encoders as Discriminators Rather Than Generators **](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/ELECTRA.pdf) [ICLR 2020] _Kevin Clark, Minh-Thang Luong, Quoc V. Le, Christopher D. Manning_.
   - Motivation: more difficult MASK
   - a little smaller MLM -> Generate random MASK -> a result
   - a discriminator if the result is correct
   - Weight Sharing -> sharing embedding & weight
   - Smaller generators
   - Training Algorithm: frozen.
6. [**Reformer: The Efficient Transformer**](https://github.com/iofu728/PaperRead/bl/master/paper/NLP/Bertology/Reformer.pdf) [ICLR 2020] _Nikita Kitaev, Lukasz Kaiser, Anselm Levskaya_.
   - LSH Mask Attention:
     - Motivation: One token should only focus on one of the few tokens.
   - indecency chunking FFN
   - single reversible copy
7. [**MPNet: Masked and Permuted Pre-training for Language Understanding**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/MPNet.pdf) [-] _Kaitao Song, Xu Tan, Tao Qin, Jianfeng Lu, Tie-Yan Liu_.
   - MLM + PLM.
   - split prediction and no-prediction.
   - make [MASK] can see other have predicted [MASK] .(condition)
   - make [MASK] can see others position.
8. [**MC-BERT: Efficient Language Pre-Training via a Meta Controller**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/MC-BERT.pdf) [-] _Zhenhui Xu, Linyuan Gong, Guolin Ke, Di He, Shuxin Zheng, Liwei Wang, Jiang Bian, Tie-Yan Liu_.
   - Probing why ELECTRA is good?
     - higher sample efﬁciency. ELECTRA-simple
     - reduced task complexity. ELECTRA-complexity(which is significantly, but why MC-BERT add the complexity, conciliatory?)
   - ELECTRA not good at semantic task.
   - K choice

## Multi-modality Bert

1. [CodeBERT: A Pre-Trained Model for Programming and Natural Languages](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/CodeBERT.pdf) [-] _Zhangyin Feng, Daya Guo, Duyu Tang, Nan Duan, Xiaocheng Feng, Ming Gong, Linjun Shou, Bing Qin, Ting Liu, Daxin Jiang, Ming Zhou_.
   - PL + NL
   - MLM + RDT(Replaced Token Detection)

## BERT Downstream

1. [**Multi-Stage Document Ranking with BERT**](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Rank/DuoBert.pdf) [-] _Rodrigo Nogueira, Wei Yang, Kyunghyun Cho, Jimmy Lin_.
   - Recall-Ranking.
   - Multi-stage add pairwise information.
