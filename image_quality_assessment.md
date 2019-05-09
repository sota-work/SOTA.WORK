# 图像质量评估

## 描述

图像质量（通常是图像质量评估，IQA）是图像的特征，其测量感知的图像劣化（通常与理想或完美图像相比）。在计算机视觉中，它可以比较分辨率，模糊，噪声等，并使用回归/分类来作出判断。

通常的评估指标是：

- 线性相关系数（LCC）：LCC衡量地面实况与预测质量得分之间的线性相关性
- Spearman等级相关系数（SROCC）：SROCC测量地面实况与估算之间的单调关系

*请参阅此处（<https://arxiv.org/abs/1707.08347>）

## 结果

### LIVE — 测试集

| Model  | LCC   | SROCC | Weights                                                      | Paper                                     | Code                                          |
| ------ | ----- | ----- | ------------------------------------------------------------ | ----------------------------------------- | --------------------------------------------- |
| VGG-16 | 0.973 | 0.974 | [Caffe](https://github.com/xialeiliu/RankIQA/blob/master/pre-trained) | [paper](https://arxiv.org/abs/1707.08347) | [Caffe](https://github.com/xialeiliu/RankIQA) |

### TID 2013 — 测试集

| Model  | LCC  | SROCC | Weights                                                      | Paper                                     | Code                                          |
| ------ | ---- | ----- | ------------------------------------------------------------ | ----------------------------------------- | --------------------------------------------- |
| VGG-16 | N/A  | 0.780 | [Caffe](https://github.com/xialeiliu/RankIQA/blob/master/pre-trained) | [paper](https://arxiv.org/abs/1707.08347) | [Caffe](https://github.com/xialeiliu/RankIQA) |

