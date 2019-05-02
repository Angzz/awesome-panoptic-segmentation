# Awesome-Panoptic-Segmentation
This repo is a collection of the challenging panoptic segmentation, including papers, codes, and benchmark results, etc.

## Panoptic Segmentation
<div align="center" width="200" height="100"><img src="img/panoptic_segmentation_overview.png"></div>
Summarize in one sentence : Panoptic Segmentation proposes to solve the semantic segmentation(*Stuff*) and instance segmentation(*Thing*) in a unified and general manner.

## Datasets

Generally, the datasets which contains both semantic and instance annotations can be used to solve the challenging *panoptic* task;  
* [Cityscapes](https://www.cityscapes-dataset.com/)
* [Mapillary Vistas](https://blog.mapillary.com/product/2017/05/03/mapillary-vistas-dataset.html)
* [ADE20K](http://groups.csail.mit.edu/vision/datasets/ADE20K/)
* [COCO-Panoptic](http://cocodataset.org/)
* [BDD100K](https://bair.berkeley.edu/blog/2018/05/30/bdd/) (the instance annotations are temporaily not released)

## Benchmark Results
* ``PQ`` are the standard metrics described in [Panoptic Segmentation](https://arxiv.org/pdf/1801.00868.pdf).
<div align="center" width="100" height="50"><img src="img/pq_metric.png"></div>

* ``PC`` are the standard metrics described in [DeeperLab](https://arxiv.org/pdf/1902.05093).
<div align="center" width="100" height="50"><img src="img/pc_metric.png"></div>

* **COCO Benchmark**
| Method | Backbone | PQ | PQ-Thing | PQ-Stuff | mIoU | AP-Mask | PC |  e2e | 
| Panoptic FPN | ResNet-101 | 40.9 | 48.3 | 29.7 | - | - | - | :heavy_check_mark: |
| UPSNet | ResNet-101 | 42.5 | 48.6 | 33.4 | 54.3 | 34.3 | - | :heavy_check_mark: |
| AUNet | ResNet-101 | 45.2 | 54.4 | 31.3 | - | - | - | :heavy_check_mark: |
| DeeperLab | Xception-71 | 33.9 | - | - | - | - | 56.82 |  :heavy_check_mark: |
| OANet | ResNet-101 | 41.3 | 50.4 | 27.7 | - | - | - | :heavy_check_mark: |

* **Cityscapes Benchmark**
| Method | Backbone | PQ | PQ-Thing | PQ-Stuff | mIoU | AP-Mask | PC |  e2e | 
| Panoptic FPN | ResNet-101 | 40.9 | 48.3 | 29.7 | - | - | - | :heavy_check_mark: |
| UPSNet | ResNet-101 | 42.5 | 48.6 | 33.4 | 54.3 | 34.3 | - | :heavy_check_mark: |
| AUNet | ResNet-101 | 45.2 | 54.4 | 31.3 | - | - | - | :heavy_check_mark: |
| DeeperLab | Xception-71 | 33.9 | - | - | - | - | 56.82 |  :heavy_check_mark: |
| OANet | ResNet-101 | 41.3 | 50.4 | 27.7 | - | - | - | :heavy_check_mark: |

* **Mapillary Benchmark** 
| Method | Backbone | PQ | PQ-Thing | PQ-Stuff | mIoU | AP-Mask | PC |  e2e | 
| Panoptic FPN | ResNet-101 | 40.9 | 48.3 | 29.7 | - | - | - | :heavy_check_mark: |
| UPSNet | ResNet-101 | 42.5 | 48.6 | 33.4 | 54.3 | 34.3 | - | :heavy_check_mark: |
| AUNet | ResNet-101 | 45.2 | 54.4 | 31.3 | - | - | - | :heavy_check_mark: |
| DeeperLab | Xception-71 | 33.9 | - | - | - | - | 56.82 |  :heavy_check_mark: |
| OANet | ResNet-101 | 41.3 | 50.4 | 27.7 | - | - | - | :heavy_check_mark: |


## Papers 
### CVPR2019
* **Panoptic Segmentation:** Alexander Kirillov, Kaiming He, Ross Girshick, Carsten Rother, Piotr Dollár.<br />"Panoptic Segmentation." CVPR (2019). [[paper](https://arxiv.org/pdf/1801.00868.pdf)]

* **Panoptic FPN:** Alexander Kirillov, Ross Girshick, Kaiming He, Piotr Dollár.<br />"Panoptic Feature Pyramid Networks." CVPR (2019 **oral**). [[paper](https://arxiv.org/pdf/1901.02446.pdf)]

* **AUNet:** Yanwei Li, Xinze Chen, Zheng Zhu, Lingxi Xie, Guan Huang, Dalong Du, Xingang Wang.<br />"Attention-guided Unified Network for Panoptic Segmentation." CVPR (2019). [[paper](https://arxiv.org/pdf/1812.03904.pdf)]

* **UPSNet:** Yuwen Xiong, Renjie Liao, Hengshuang Zhao, Rui Hu, Min Bai, Ersin Yumer, Raquel Urtasun.<br />"UPSNet: A Unified Panoptic Segmentation Network." CVPR (2019). [[paper](https://arxiv.org/pdf/1901.03784.pdf)] [[code](https://github.com/uber-research/UPSNet)]

* **DeeperLab:** Tien-Ju Yang, Maxwell D. Collins, Yukun Zhu, Jyh-Jing Hwang, Ting Liu, Xiao Zhang, Vivienne Sze, George Papandreou, Liang-Chieh Chen.<br />"DeeperLab: Single-Shot Image Parser." CVPR (2019). [[paper](https://arxiv.org/pdf/1902.05093)] [[project](http://deeperlab.mit.edu)] [[code](https://github.com/tensorflow/models/tree/master/research/deeplab/evaluation)]

* **TASCNet:** Jie Li, Allan Raventos, Arjun Bhargava, Takaaki Tagawa, Adrien Gaidon.<br />"Learning to Fuse Things and Stuff." CVPR (2019). [[paper](https://arxiv.org/pdf/1812.01192)]

* **OANet:** Huanyu Liu, Chao Peng, Changqian Yu, Jingbo Wang, Xu Liu, Gang Yu, Wei Jiang.<br />"An End-to-End Network for Panoptic Segmentation." CVPR (2019). [[paper](https://arxiv.org/pdf/1903.05027.pdf)]

* Eirikur Agustsson, Jasper R. R. Uijlings, Vittorio Ferrari
.<br />"Interactive Full Image Segmentation by Considering All Regions Jointly." CVPR (2019). [[paper](https://arxiv.org/pdf/1812.01888.pdf)]


### ECCV2018
* Qizhu Li, Anurag Arnab, Philip H.S. Torr.<br />"Weakly- and Semi-Supervised Panoptic Segmentation." ECCV (2018). [[paper](https://arxiv.org/pdf/1812.01192.pdf)] [[code](https://github.com/qizhuli/Weakly-Supervised-Panoptic-Segmentation)]

### ArXiv

* Daan de Geus, Panagiotis Meletis, Gijs Dubbelman.<br />"Panoptic Segmentation with a Joint Semantic and Instance Segmentation Network." arXiv (2018). [[paper](https://arxiv.org/pdf/1809.02110.pdf)]

* Daan de Geus, Panagiotis Meletis, Gijs Dubbelman.<br />"Single Network Panoptic Segmentation for Street Scene Understanding." arXiv (2019). [[paper](https://arxiv.org/pdf/1902.02678.pdf)]

* David Owen, Ping-Lin Chang.<br />"Detecting Reflections by Combining Semantic and Instance Segmentation." arXiv (2019). [[paper](https://arxiv.org/pdf/1904.13273.pdf)]

* Gaku Narita, Takashi Seno, Tomoya Ishikawa, Yohsuke Kaji.<br />"PanopticFusion: Online Volumetric Semantic Mapping at the Level of Stuff and Things." arXiv (2019). [[paper](https://arxiv.org/pdf/1903.01177.pdf)]

