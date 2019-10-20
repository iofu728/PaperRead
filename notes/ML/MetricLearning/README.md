# Metric Learning

1. [**Constellation Loss: Improving the efﬁciency of deep metric learning loss functions for optimal embedding.**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/ConstellationLoss.pdf) [NIPS] _Alfonso Medela, Artzai Picon_.
   - when we use the multi-class n pair loss, the num of negative is fixed. because of using the the same class to be the negative sample.
   - And the controlled parameters K, means we can change the computational effort in the model.
2. [**FaceNet: A Uniﬁed Embedding for Face Recognition and Clustering**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/FaceNet.pdf) [CVPR 2015] _Florian Schroff, Dmitry Kalenichenko, James Philbin_.
   - a unified embedding for Recognition and Clustering
   - Triple Loss to align the distance between Position sample and negative sample
   - online negative sample mining strategy
3. [**Beyond triplet loss: a deep quadruplet network for person re-identification**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/QuadrupletLoss.pdf) [CVPR 2017] _Weihua Chen, Xiaotang Chen, Jianguo Zhang, Kaiqi Huang_.
   - large inter-class variation + small intra-class variation
   - $$\begin{aligned} L_{q u a d}=& \sum_{i, j, k}^{N}\left[g\left(x_{i}, x_{j}\right)^{2}-g\left(x_{i}, x_{k}\right)^{2}+\alpha_{1}\right]_{+} \\ &+\sum_{i, j, k, l}^{N}\left[g\left(x_{i}, x_{j}\right)^{2}-g\left(x_{l}, x_{k}\right)^{2}+\alpha_{2}\right]_{+} \\ & s_{i}=s_{j}, s_{l} \neq s_{k}, s_{i} \neq s_{l}, s_{i} \neq s_{k} \end{aligned}$$
4. [**Improved Deep Metric Learning with Multi-class N-pair Loss Objective**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/Multi-classN-pairLoss.pdf) [CVPR 2016] _Kihyuk Sohn_.
   - $$\mathcal{L}_{N-\text { pair me }}\left(\left\{\left(x_{i}, x_{i}^{+}\right)\right\}_{i=1}^{N} ; f\right)=\frac{1}{N} \sum_{i=1}^{N} \log \left(1+\sum_{j \neq i} \exp \left(f_{i}^{\top} f_{j}^{+}-f_{i}^{\top} f_{i}^{+}\right)\right)$$
5. [**Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/SentenceBert.pdf) [EMNLP 2019] _Nils Reimers, Iryna Gurevych_.
   - reduce similar computational in STS.
   - three pooling strategy
     - CLS-token
     - max strategy
     - mean strategy
   - three objective function
     - classification objective function
     - regression objective function
     - triplet objective function
