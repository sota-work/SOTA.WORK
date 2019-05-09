# ADE20K

### 描述

- [场景解析ADE20K数据集](http://people.csail.mit.edu/bzhou/publication/scene-parse-camera-ready.pdf)
- [通过ADE20K数据集对场景进行语义理解](https://arxiv.org/pdf/1608.05442.pdf)
- [官方网站](http://groups.csail.mit.edu/vision/datasets/ADE20K/)

使用ADE20K数据的挑战：

- [麻省理工学院场景解析基准（2016）](http://sceneparsing.csail.mit.edu/)
- [地方挑战赛（ICCV 2017）](http://placeschallenge.csail.mit.edu/)

评估通常在竞赛框架内进行。对于场景分析和场所中的目标度量，作者使用像素精度和平均交叉点的平均值。

### 下载

#### 原装ADE20K

- [完整数据集（3.8G .zip）](http://groups.csail.mit.edu/vision/datasets/ADE20K/ADE20K_2016_07_26.zip)

#### 麻省理工学院场景解析挑战

数据来自原始ADE20K数据集

- [训练集/验证集](http://data.csail.mit.edu/places/ADEchallenge/ADEChallengeData2016.zip)
- [测试集](http://data.csail.mit.edu/places/ADEchallenge/release_test.zip)

### 技术细节

- **训练集中的** 210个图像，**验证集中的** 2000个图像，**测试集中的** 3000个图像。
- 20个对象类和434 826个对象实例。
- 超过20个对象类的更精细的分层标签：150个填充/对象标签（例如墙，天空，树）和1038个图像级标签（例如机场终端，卧室，街道）
- 不同的空间分辨率：中值图像大小 - 307 200像素，中值纵横比为1.33。

### 格式

每个文件夹包含按场景类别分隔的图像（与场所数据库相同的场景类别）。对于每个图像，对象和部分分割存储在两个不同的png文件中。所有对象和零件实例都可以进行注释。

对于每个图像，有以下文件：

##### * .JPG

输入RGB图像。

##### * _seg.png

RGB图像与对象分割掩码。掩码具有以下结构：

##### * _seg_parts_N.png

零件分割掩码，其中N是一个数字（1,2,3，...），表示零件层次结构中的级别。N = 1 - 对象的一部分。由于N可以> 1，零件也可以由零件组成。

##### *_.文本

描述每个图像内容的文本文件（描述对象和部分）。此信息与其他文件一样多余。但另外还包含有关对象属性的信息。`loadAde20K.m`官方工具包中提供的功能（见下文）也解析了该文件的内容。文本文件中的每一行包含六列，其中包含以下内容：

1. 实例编号
2. 零件级别（对象为0）
3. 遮挡指标（1表示真实）
4. 类名（使用wordnet解析）
5. 原始原始名称（可能提供更详细的分类）
6. 逗号分隔的属性列表

### 资源

| 链接                                                         | 描述                            |
| ------------------------------------------------------------ | ------------------------------- |
| [ADE20K的分段模型（PyTorch）](https://github.com/CSAILVision/semantic-segmentation-pytorch) | PyTorch实现了分段模型和训练例程 |
| [MATLAB开发套件](https://github.com/CSAILVision/sceneparsing) | 评估/可视化脚本                 |
| [麻省理工学院团队的基线](https://github.com/CSAILVision/sceneparsing/wiki/Model-Zoo) | 一堆预先训练的PyTorch模型       |
| [用于加载的官方MATLAB工具](http://groups.csail.mit.edu/vision/datasets/ADE20K/code.zip) | 用于加载和浏览数据的MATLAB脚本  |

### 演示

具有相应对象级（第2行）和部分级（第3行）分段的图像样本（第1行）：

[高分辨率样本](http://groups.csail.mit.edu/vision/datasets/ADE20K/assets/images/examples.png)

基于Web的工具，用于浏览不同的数据拆分：

- [训练集](http://sceneparsing.csail.mit.edu/browse.php/?dirname=training/)
- [验证集](http://sceneparsing.csail.mit.edu/browse.php/?dirname=validation/)