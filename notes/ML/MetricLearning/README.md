# Metric Learning

1. [Constellation Loss: Improving the efﬁciency of deep metric learning loss functions for optimal embedding.](https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/ConstellationLoss.pdf) [NIPS] Alfonso Medela, Artzai Picon.
   - when we use the multi-class n pair loss, the num of negative is fixed. because of using the the same class to be the negative sample.
   - And the controlled parameters K, means we can change the computational effort in the model.
2. [FaceNet: A Uniﬁed Embedding for Face Recognition and Clustering](https://github.com/iofu728/PaperRead/blob/master/paper/ML/MetricLearning/FaceNet.pdf) [CVPR 2015] Florian Schroff, Dmitry Kalenichenko, James Philbin.
   - a unified embedding for Recognition and Clustering
   - Triple Loss to align the distance between Position sample and negative sample
   - online negative sample mining strategy
