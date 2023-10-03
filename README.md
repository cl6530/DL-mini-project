# Modified residual network (ResNet) architecture with the high test accuracy on the CIFAR- 10 image classification dataset
In this project, our goal is to develop a lightweight version of ResNet (Zhang, Ren and Sun 2015) for image classification tasks. We achieved this by modifying the residual block within ResNet, resulting in a significant reduction in the number of parameters without sacrificing much of the model’s capability. Additionally, we employed various preprocessing techniques, such as normalization and data augmentation, to enhance performance and achieve faster con- vergence. Finally, we experimented with multiple combina- tions of model parameters and optimizer to obtain an optimal model. As a result, we achieved a prediction accuracy of 91.47% on the CIFAR-10 (Krizhevsky and Hinton 2009) dataset with approximately 2.8 million trainable parameters. The codebase could be found through this publicly accessible github repository (https://github.com/TigaJi/DL-mini-project). (Ji, Liu and Douglas 2023)
| **Model** | **Batch Size(training)** | **Batch Size(testing)** | **Optimizer** | **lr** | **#residual layer** | **#epoch** | **#params** | **Acc(%)** |
|-----------|--------------------------|-------------------------|---------------|--------|---------------------|------------|-------------|------------|
| 0         | 512                      | 512                     | Adam         | 0.01   | 5                   | 70         | 4,587,306   | 91.28      |
| 1         | 128                      | 128                     | Adam         | 0.01   | 5                   | 70         | 4,587,306   | 91.23      |
| 2         | 512                      | 512                     | SGD          | 0.01   | 5                   | 70         | 4,587,306   | 83.25      |
| 3         | 256                      | 256                     | Adam         | 0.01   | 5                   | 70         | 4,587,306   | 90.97      |
| 4         | 256                      | 128                     | Adam         | 0.01   | 5                   | 70         | 4,587,306   | 90.90      |
| **5**     | **128**                  | **128**                 | **Adam**     | **0.01** | **4**             | **70**     | **2,799,146** | **91.47** |
| 6         | 128                      | 128                     | Adam         | 0.1    | 5                   | 70         | 4,587,306   | 88.87      |
| 7         | 128                      | 128                     | Adam         | 0.001  | 5                   | 70         | 4,587,306   | 91.14      |
| 8         | 128                      | 128                     | Adam         | 0.01   | 4                   | 70         | 4,367,786   | 91.24      |
