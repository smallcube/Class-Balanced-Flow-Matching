# Class-Balanced-Flow-Matching
Try to train Flow Matching under long-tailed data distribution

# reference work
(1) ICLR 24-[Long-tailed Diffusion Models with Oriented Calibration](https://proceedings.iclr.cc/paper_files/paper/2024/file/7dff60c3db3c0d2f3acf92f13b1b2472-Paper-Conference.pdf)

(2) CVPR 25-[Image Generation Diversity Issues and How to Tame Them](https://www.openaccess.thecvf.com/content/CVPR2025/papers/Dombrowski_Image_Generation_Diversity_Issues_and_How_to_Tame_Them_CVPR_2025_paper.pdf)

(3) ECCV 26-[Contrastive Conditional–Unconditional Alignment for Long-Tailed Diffusion Model](https://link.springer.com/chapter/10.1007/978-3-032-37520-9_23)

(4) NIPS 25-[CORAL: Disentangling Latent Representations in Long-Tailed Diffusion](https://proceedings.neurips.cc/paper_files/paper/2025/file/a32539cb16274581a17e679f6046f4bf-Paper-Conference.pdf)

(5) ICML 25-[Boost-and-skip: a simple guidance-free diffusion for minority generation](https://arxiv.org/pdf/2502.06516)

(6) CVPR 25-[Image Generation Diversity Issues and How to Tame Them](https://www.openaccess.thecvf.com/content/CVPR2025/papers/Dombrowski_Image_Generation_Diversity_Issues_and_How_to_Tame_Them_CVPR_2025_paper.pdf)

(7) TIP 24-[Rethinking Noise Sampling in Class-Imbalanced Diffusion Models](https://drive.google.com/file/d/1qwxC48t4i7JUM9Yn2odepdf5zGrma_DK/view?pli=1)

(8) ICLR 24-[LABEL-NOISE ROBUST DIFFUSION MODELS](https://proceedings.iclr.cc/paper_files/paper/2024/file/911ac8327812e919f97d36f4d08fd5f4-Paper-Conference.pdf)

(9) ICLR 26-[IMPROVING DIFFUSION MODELS FOR CLASSIMBALANCED TRAINING DATA VIA CAPACITY MANIPULATION](https://openreview.net/pdf?id=wSGle6ag5I)

(10) CVPR25-[Minority-Focused Text-to-Image Generation via Prompt Optimization](https://openaccess.thecvf.com/content/CVPR2025/papers/Um_Minority-Focused_Text-to-Image_Generation_via_Prompt_Optimization_CVPR_2025_paper.pdf)

(11) ICLR 24-[Don't Play Favorites: Minority Guidance for Diffusion Models](https://proceedings.iclr.cc/paper_files/paper/2024/file/5dc387343572bb95f264e05b66e83951-Paper-Conference.pdf)

(12) ICLR 25-[TFG-Flow: Training-free Guidance in Multimodal Generative Flow](https://proceedings.iclr.cc/paper_files/paper/2025/file/aca042ae71283d25b3d063fc011db9e8-Paper-Conference.pdf)

(13) ICML 26-[Calibrating Generative Models to Distributional Constraints](https://openreview.net/pdf?id=5yXKRaNI2R)

(14)


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
