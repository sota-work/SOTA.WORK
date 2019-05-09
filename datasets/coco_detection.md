# COCO数据集2016 - 检测

### 描述

- [Microsoft COCO：上下文中的常见对象](https://arxiv.org/abs/1405.0312)
- [上下文中的常见对象](http://cocodataset.org/)

挑战使用了几个指标，但通常报告的是：

- **平均精度**
- **平均精度@ 0.5,0.75 IoU，**对于具有> = 0.5 IoU且具有基本事实的边界框上的标签 - 主要度量。
- **AP-small** - AP用于区域（总像素）<1024的实例
- **AP-medium** - AP为1024 <= area <9216的实例
- **AP-large** - AP用于面积> = 9216的实例

### 下载

- [训练图像](http://images.cocodataset.org/zips/train2014.zip)
- [验证图像](http://images.cocodataset.org/zips/val2014.zip)
- [训练/ 测试集注解](http://images.cocodataset.org/annotations/annotations_trainval2014.zip)
- [测试图像](http://images.cocodataset.org/zips/test2015.zip)
- [测试图像信息](http://images.cocodataset.org/annotations/image_info_test2015.zip)

### 技术细节

- 训练集：~83000图像，604907个实例
- 验证集：~41000张图片
- 80个分类加入了12个超类别
- 像素数：90％的图像在列车组中具有167500和355840像素之间。
- 高/宽比：90％的图像在列车组中的比率在0.6和1.5之间。
- 实例数：99％的图像包含1到33个不同的实例，中位数= 4（训练集）。

### 格式

目标标签包含在单独的JSON文件中。边框和相应的标签在`instances_train2014.json`和中提供`instances_val2014.json`。

实例注释存储`annotations`在相应文件中的键下的列表中。每个对象包含一个图像中一个实例的注解。对于检测任务，以下字段特别重要：

- `image_id`：数据库中输入图像的ID
- `bbox`：4元组包含矩形边界框的关键点
- `category_id`：与实例关联的类的数量

可以在密钥下找到有关类别的信息，例如名称和ID `categories`。可以在密钥下找到有关图像的信息（文件名，分辨率，ID，区域）`images`。

数据集的维护者提供了一个多语言API（如下所列），用于处理整个数据库的索引。

### 资源

指向提取/转换/可视化的辅助脚本的链接。

| 链接                                               | 描述                                          |
| -------------------------------------------------- | --------------------------------------------- |
| [COCO API](https://github.com/cocodataset/cocoapi) | 用于处理COCO数据集的Lua，Matlab和Python API。 |