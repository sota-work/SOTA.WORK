# PASCAL VOC 2012 - 细分

### 描述

- [论文](https://link.springer.com/content/pdf/10.1007/s11263-009-0275-4.pdf)
- [网站](http://host.robots.ox.ac.uk/pascal/VOC/voc2012/htmldoc/devkit_doc.html#SECTION00060000000000000000)
- [评估服务器（需要注册）](http://host.robots.ox.ac.uk:8080/)

RGB图像具有相应的逐像素注释。图像包含逼真的日常场景。

对于评估，通常的度量是平均交叉联盟（mIoU）。

### 下载

- [训练和验证集](http://host.robots.ox.ac.uk/pascal/VOC/voc2012/VOCtrainval_11-May-2012.tar)

### 技术细节

可用数据分为**列**和**val**集，分别包含1464和1449个图像。

- 20类标签+背景+未标记
- 中位数像素数：187500,90％的图像具有147000到200000像素
- 中值高宽比为0.75,90％的图像在0.66和1.5之间。

### 资源

指向提取/转换/可视化的辅助脚本的链接。

| 链接                                                         | 描述                       |
| ------------------------------------------------------------ | -------------------------- |
| [数据集脚本](https://github.com/warmspringwinds/tf-image-segmentation/blob/master/tf_image_segmentation/utils/pascal_voc.py) | Python中的一组实用程序函数 |