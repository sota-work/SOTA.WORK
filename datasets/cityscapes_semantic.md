# 城市风景 - 语义分割

### 描述

- [城市景观数据集对语义城市场景的理解](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Cordts_The_Cityscapes_Dataset_CVPR_2016_paper.pdf)
- [官方网站](https://www.cityscapes-dataset.com/)

使用数据集和评估端点访问归档都位于[挑战的网站上](https://www.cityscapes-dataset.com/)。

使用class-mIoU，category-mIoU，instance mIoU和pixel precision accuracy来评估分割模型的性能。

### 技术细节

- 训练/验证/测试集分别分成2975,500和1525个图像。
- 每张图片的大小为1024x2048。
- 数据集包含19个对象类和其他实例级标签。

### 格式

训练集和验证集包含输入RGB图像，这些图像由以下列方式组织的单独文件中的标签补充：

每个文件夹包含按场景类别分隔的图像（与场所数据库相同的场景类别）。对于每个图像，对象和部分分割存储在两个不同的png文件中。所有对象和零件实例都可以进行注释。

对于每个图像，有以下文件：

##### * _leftImg8bit.png

输入RGB图像。

##### * _gtFine_labelIds.png

RGB图像与对象分割掩码。每个像素由单字节无符号整数表示，表示正确的类标签。在培训期间应忽略某些课程。

### 工具

指向提取/转换/可视化的辅助脚本的链接。

| 链接                                                         | 描述                             |
| ------------------------------------------------------------ | -------------------------------- |
| [城市风景脚本](https://github.com/mcordts/cityscapesScripts) | 用于检查，准备和评估的脚本集合。 |