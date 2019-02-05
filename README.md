# Deep Co-Training for Semi-Supervised Image Recognition

This is the unofficial PyTorch implementation of the paper "Deep Co-Training for Semi-Supervised Image Recognition" in ECCV 2018. 
It only contains the code for 2-view co-training on CIFAR-10.
The repository is maintained by Hsin-Ping Chou and Jie-Young Chen.

## Overview

All hyperparameters are set the same as they are mentioned in the paper. There are two things that are not mentioned in the paper. One is the epsilon of the FGSM attack. 
The other one is how they attack those unlabelled data. We've asked the authors of the paper and got their response. The epsilon was set to 0.02 and they used the pseudo label of those 
unlabelled data to attack. Note that for FGSM attack. The authors of the paper also mentioned that they didn't use torch.clamp which is usually used for FGSM.

We've tested the code with PyTorch version 0.4.1 and Python 3.5. It can achieve % error rate with a single 1080ti GPU in which is still far from the reported baseline in the paper.
