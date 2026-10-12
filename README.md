# Class-Balanced-Flow-Matching
Try to train Flow Matching under long-tailed data distribution



# 2026-10-10 下一步工作安排：
（1）急迫任务：Flow Matching在ImageNet-LT上的标准FID和IS等指标；
（2）如果算力告警，可以使用CIFAR-100-LT进行基础实验；
（3）确保Classifier-free方案能够跑出一个可用的生成模型；


# 2026-09-18 下一步工作安排：
（1）在ImageNet-Lt 上跑通 Flow Matching，包括：classifier-guidance和classifier-free两种方案，以及两种方案对应的基准FiD和IS。
（2）Classifier-guidance= unconditional Flow Matching + Classifier
（3）Classifier-free = conditional Flow Matching + Text Encoder (CLIP)


classifier-free guidance方案中可供优化的点：
（1）优化cross attention，可供借鉴的地方：现有文献中对cross attention的改进；
 (2) 优化采样过程，根据数据的不平衡分布或者梯度信息，优化不同类别向量v的大小和方向；
（3）借鉴class-balanced diffusion model，对训练的loss进行改进；
