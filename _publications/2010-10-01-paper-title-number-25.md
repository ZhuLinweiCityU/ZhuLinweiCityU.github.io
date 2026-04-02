---
title: "[IEEE T-MM 2026] Temporal Consistency-Aware Dynamic Point Clouds Color Attribute Enhancement"
collection: publications
permalink: /publication/2010-10-01-paper-title-number-25
excerpt: '**Linwei Zhu**, Ruxu Liang, Yun Zhang#, Hui Yuan, and Sam Kwong, “Temporal Consistency-Aware Dynamic Point Clouds Color Attribute Enhancement”, IEEE Transactions on Multimedia (IEEE T-MM), accepted, to be published, 2026. [paper](https://ieeexplore.ieee.org/document/11340745)'
date: 2026-04-01
venue: 'IEEE Transactions on Multimedia (IEEE T-MM)'
---
**Linwei Zhu**, Ruxu Liang, Yun Zhang, Hui Yuan, and Shiqi Wang, “Temporal Consistency-Aware Dynamic Point Clouds Color Attribute Enhancement”, IEEE Transactions on Multimedia (IEEE T-MM), accepted, to be published, 2026. [paper](https://ieeexplore.ieee.org/document/11340745)

<br/><img src='/images/DPC.jpg'>

聚焦动态点云压缩后的颜色属性增强问题，提出了一种时间一致性感知的动态点云颜色属性增强方法，有效解决了压缩量化导致的失真尤其是时间不一致性问题，相关源码和训练模型已开源，研究成果在性能上优于当前主流方法。 

研究背景与问题 
动态点云是虚拟现实、自动驾驶等领域的重要数据载体，但在压缩过程中的量化操作会产生显著失真，其中时间不一致性问题尤为突出，严重降低了动态点云的视觉质量，成为制约其实际应用的关键痛点，现有方法尚未能有效兼顾时空维度的特征关联与颜色属性修复。 

核心方法设计 
论文构建了由三大核心模块组成的增强框架，从时空特征对齐、单帧特征提取、时空依赖捕捉三个维度实现颜色属性优化： 1. 3D 时空搜索（3D Spatial-Temporal Search, STS）模块：在时间域内自适应搜索点云块，完成跨帧的特征对齐，为后续特征提取奠定时空匹配基础； 2. 单帧特征提取（Single Frame Feature Extraction, SFFE）模块：融合多头注意力机制与图卷积网络，对经 STS 模块匹配后的点云块单独处理，充分挖掘点云颜色属性的潜在特征； 3. 卷积点云长短期记忆（Conv-PointLSTM）网络：将卷积、最大池化与 LSTM 机制结合，进一步捕捉点云在空间和时间维度的双重依赖关系，实现时空潜在特征间的颜色属性关联匹配。  

实验结果与性能 
该方法经实验验证展现出优异的性能，相比当前主流技术实现显著提升： • 峰值信噪比（PSNR）平均提升0.44 dB，直接改善了动态点云的视觉质量； • 在低码率下实现1.50% 的码率降低，高码率下码率降低幅度达5.31%，在保证视觉效果的同时提升了压缩效率。  

研究价值与开源信息 
论文提出的方法为动态点云压缩后的质量增强提供了新的解决方案，其核心创新在于将时空一致性感知融入颜色属性修复，兼顾了特征的空间挖掘与时间关联。相关源码和训练模型已开源至 GitHub（https://github.com/xu-coder-666/DPC），为该领域的后续研究和工程应用提供了可复现的技术支撑。