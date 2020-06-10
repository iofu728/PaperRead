# Multi-task

1. [**Learning without Forgetting**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Multi-task/LearningWithoutForgot.pdf) [ECCV 2016] _Zhizhong Li, Derek Hoiem_.
   - Train multi-task model in no old dataset.
   - Distillation and fine-tuning.
     - task-specific layers
     - network expansion
     - lower lr
     - loss
2. [**Dynamic Task Prioritization for Multitask Learning**](https://github.com/iofu728/PaperRead/bl/master/paper/ML/Multi-task/DynamicTaskPrioritizationForMultiTask.pdf) [ECCV 2018] _Michelle Guo, Albert Haque, De-An Huang, Serena Yeung, Li Fei-Fei_.
   - Using Focal Loss Control the prioritization of different tasks.
   - using KPIs(like acc) to evaluate the sample hard degree.
   - give hard sample higher priority.
3. [**SNR: Sub-Network Routing for Flexible Parameter Sharing in Multi-Task Learning**](https://github.com/iofu728/PaperRead/blob/master/paper/ML/Multi-task/SNR.pdf) [AAAI 2019] _J Ma, Z Zhao, J Chen, A Li, L Hong, EH Chi_.
   - flexible connection of previous block in different task.
   - like a binary encoding.
   - To learn the (0, 1) weight, they follow the Louizos's work which relaxation to smooth such objective functions so that can directly calculate the gradients of the distribution parameters.
