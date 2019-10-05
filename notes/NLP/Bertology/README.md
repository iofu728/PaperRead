# Bertology

1. [ALBERT: A L ITE BERT FOR S ELF - SUPERVISED L EARNING OF L ANGUAGE R EPRESENTATIONS](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/ALBert.pdf)[submit ICLR 2020] Anonymous authors.

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

2. [Unified Language Model Pre-training for Natural Language Understanding and Generation](https://github.com/iofu728/PaperRead/blob/master/paper/NLP/Bertology/UniLM.pdf) [-] Li Dong, Nan Yang, Wenhui Wang, Furu Wei, Xiaodong Liu, Yu Wang, Jianfeng Gao, Ming Zhou, Hsiao-Wuen Hon.
   - three mask
     - unidirectional
     - bidirectional
     - seq2seq
   - framework support both NLU & NLG
