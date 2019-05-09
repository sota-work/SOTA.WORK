# 物体检测

## 描述

这些问题被公式化为预测带有输入图像中每个对象的相应类标签的边界框。每个图像可以包含多个对象。

两个主要指标是平均精度（mAP）和平均平均召回（mAR）。有关竞争特定指标的其他信息，请参阅数据集说明。

## 结果

### MS-COCO 2016

[数据集描述](datasets/coco_detection.md)

结果来自[Google Research Model Zoo](https://github.com/tensorflow/models/tree/master/research/object_detection)

除了每个模型的mAP之外，我们还在冻结推理图中包含每个图像的推理时间（以毫秒为单位）。

| Model                            | mAP, % | Inference time, ms | Weights                                                      | Paper                                     | Code                                                         |
| -------------------------------- | ------ | ------------------ | ------------------------------------------------------------ | ----------------------------------------- | ------------------------------------------------------------ |
| Faster R-CNN NasNet              | 43     | 1833               | [TensorFlow](http://download.tensorflow.org/models/object_detection/faster_rcnn_nas_coco_2018_01_28.tar.gz) | [paper](https://arxiv.org/abs/1506.01497) | [TensorFlow](https://github.com/tensorflow/models/blob/master/research/object_detection/meta_architectures/faster_rcnn_meta_arch.py) |
| Faster R-CNN Inception-ResNet-v2 | 37     | 771                | [TensorFlow](http://download.tensorflow.org/models/object_detection/mask_rcnn_inception_resnet_v2_atrous_coco_2018_01_28.tar.gz) | [paper](https://arxiv.org/abs/1506.01497) | [TensorFlow](https://github.com/tensorflow/models/blob/master/research/object_detection/meta_architectures/faster_rcnn_meta_arch.py) |
| Faster R-CNN ResNet-101          | 32     | 470                | [TensorFlow](http://download.tensorflow.org/models/object_detection/faster_rcnn_resnet101_coco_2018_01_28.tar.gz) | [paper](https://arxiv.org/abs/1506.01497) | [TensorFlow](https://github.com/tensorflow/models/blob/master/research/object_detection/meta_architectures/faster_rcnn_meta_arch.py) |
| Faster R-CNN ResNet-50           | 30     | 343                | [TensorFlow](http://download.tensorflow.org/models/object_detection/faster_rcnn_resnet50_coco_2018_01_28.tar.gz) | [paper](https://arxiv.org/abs/1506.01497) | [TensorFlow](https://github.com/tensorflow/models/blob/master/research/object_detection/meta_architectures/faster_rcnn_meta_arch.py) |
| R-FCN ResNet-101                 | 30     | 92                 | [TensorFlow](http://download.tensorflow.org/models/object_detection/rfcn_resnet101_coco_2018_01_28.tar.gz) | [paper](https://arxiv.org/abs/1605.06409) | [TensorFlow](https://github.com/tensorflow/models/blob/master/research/object_detection/meta_architectures/rfcn_meta_arch.py) |
| Faster R-CNN Inception-v2        | 28     | 58                 | [TensorFlow](http://download.tensorflow.org/models/object_detection/faster_rcnn_inception_v2_coco_2018_01_28.tar.gz) | [paper](https://arxiv.org/abs/1506.01497) | [TensorFlow](https://github.com/tensorflow/models/blob/master/research/object_detection/meta_architectures/faster_rcnn_meta_arch.py) |
| SSD Inception-v2                 | 24     | 42                 | [TensorFlow](http://download.tensorflow.org/models/object_detection/ssd_inception_v2_coco_2018_01_28.tar.gz) | [paper](https://arxiv.org/abs/1512.02325) | [TensorFlow](https://github.com/tensorflow/models/blob/master/research/object_detection/meta_architectures/ssd_meta_arch.py) |
| SSD MobileNet-v2                 | 22     | 31                 | [TensorFlow](http://download.tensorflow.org/models/object_detection/ssd_mobilenet_v2_coco_2018_03_29.tar.gz) | [paper](https://arxiv.org/abs/1512.02325) | [TensorFlow](https://github.com/tensorflow/models/blob/master/research/object_detection/meta_architectures/ssd_meta_arch.py) |
| SSD-Lite MobileNet-v2            | 22     | 27                 | [TensorFlow](http://download.tensorflow.org/models/object_detection/ssdlite_mobilenet_v2_coco_2018_05_09.tar.gz) | [paper](https://arxiv.org/abs/1512.02325) | [TensorFlow](https://github.com/tensorflow/models/blob/master/research/object_detection/meta_architectures/ssd_meta_arch.py) |
| SSD MobileNet-v1                 | 21     | 30                 | [TensorFlow](http://download.tensorflow.org/models/object_detection/ssd_mobilenet_v1_coco_2018_01_28.tar.gz) | [paper](https://arxiv.org/abs/1512.02325) | [TensorFlow](https://github.com/tensorflow/models/blob/master/research/object_detection/meta_architectures/ssd_meta_arch.py) |

## 资源

| Title                                                        | Type | Description                                                  |
| ------------------------------------------------------------ | ---- | ------------------------------------------------------------ |
| [Supercharge your Computer Vision models with the TensorFlow Object Detection API](https://ai.googleblog.com/2017/06/supercharge-your-computer-vision-models.html) | Post | Announcement of open-source object detection models releaseby Google Research |