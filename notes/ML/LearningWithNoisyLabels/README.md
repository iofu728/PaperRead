# Learning With Noisy Labels

1. [**Co-teaching: Robust Training of Deep Neural Networks with Extremely Noisy Labels**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/LearningWithNoisyLabels/Co-teaching.pdf) [NIPS 2018] _Bo Han, Quanming Yao, Xingrui Yu, Gang Niu, Miao Xu, Weihua Hu, Ivor Tsang, Masashi Sugiyama_.
   - Memorization effects: DNN first learning cleaning data, and then overfitting in noisy data.
   - Co-teaching set two same NN architectures, and simultaneously training.
   - Evert mini-batch, change small-loss updating parameters.
