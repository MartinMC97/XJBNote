### FastFCN: Rethinking Dilated Convolution in the Backbone for Semantic Segmentation

[论文地址](https://arxiv.org/abs/1903.11816)

[项目地址](https://github.com/wuhuikai/FastFCN)

- 语义分割是计算机视觉领域的基础任务之一，其目的是为图像的每个像素分配语义标签。

- 当下的语义分割的方法通常在主干网络中使用扩张卷积（dilated convolutions）的方法以提取出高分辨率的特征图，但该方法的计算复杂度和内存占用相应地偏高。

- 当前实现语义分割的方法通常是使用全卷积网络（Fully Convolution Network，FCN），完成。该方法衍生自用于图像分类的卷积神经网络（Convolutional Neural Network，CNN）。原始的 FCN 将输入的图像进行下采样工作，该过程通过跨步卷积和/或空间池化层逐步对输入图像进行下采样，从而生成低分辨率的最终特征图。最终的特征图编码了丰富的语义信息，却丢失了精细的图像结构信息，导致目标边界预测不准确。

- 为降低扩张卷积过程中时间和内存的消耗，该文章提出了一个新的联合上采样模块，称为联合金字塔形上采样（Joint Pyramid Upsampling，JPU）。该方法将提取高分辨率特征图的工作公式化为联合上采样问题。从而降低计算复杂度，缩短时间并降低内存占用。

