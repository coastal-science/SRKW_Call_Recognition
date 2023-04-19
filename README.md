# Fewshot learning algorithm Comparsion

This repository is Experment Code for Matching Network, ProtoNet, MAML and Distribution Propagation Graph Network

## Abstract
As an important branch of deep learning, few-shot Learning does not require a large amount of data but chooses a softer approach to solve problems, where it can be perfectly integrated with techniques such as meta learning and data augmentation. In this repository, I test four algorithms:Matching Network, ProtoNet, MAML and Distribution Propagation Graph NN on four FSL datasets: miniImageNet, Omniglot, CUB-200-2011 and CIFAR-FS.

## Requirements

CUDA Version: 10.1

Python : 3.6.9

To install dependencies:

```setup
sudo pip3 install -r requirements.txt
```
## Dataset
For your convenience, you can download the datasets directly from links on the left, or you can make them from scratch following the original splits on the right. 

|    Dataset    | Algorithms Paper |
| :-----------: |:----------------:|
|  [Mini-ImageNet](https://drive.google.com/open?id=15WuREBvhEbSWo4fTr1r-vMY0C_6QWv4w)  |  [Matching Networks](https://arxiv.org/pdf/1606.04080.pdf)  | 
|    [Omniglot](https://drive.google.com/file/d/1nVGCTd9ttULRXFezh4xILQ9lUkg0WZCG)   |   [ProtoNet](https://arxiv.org/abs/1803.00676)   |
|  [CIFAR-FS](https://drive.google.com/file/d/1GjGMI0q3bgcpcB_CjI40fX54WgLPuTpS)  |   [MAML](https://arxiv.org/pdf/1805.08136.pdf)   |
|      [CUB-200-2011](https://github.com/wyharveychen/CloserLookFewShot/tree/master/filelists/CUB)     |   [DP GNN](https://arxiv.org/pdf/1904.04232.pdf)   |



Experment obtained the following performance on mini-ImageNet, Omniglot, CUB-200-2011 and CIFAR-FS.

**miniImageNet**:

|     Method    |   Backbone   |   5way-1shot   |   5way-5shot   |
| :-----------: |:------------:|----------------|:--------------:|
|  MatchingNet  |    ConvNet   |   43.56±0.84   |   55.31± 0.73  |
|    ProtoNet   |    ConvNet   |   49.42±0.78   |   68.20±0.66   |
|      MAML     |    ConvNet   |   48.70±1.84   |   55.31±0.73   |
|      DPGN     |    ConvNet   | **66.01±0.36** | **82.83±0.41** |



**CUB-200-2011**:

|     Method    |   backbone   |   5way-1shot   |   5way-5shot   |
| :-----------: |:------------:|----------------|:--------------:|
|      MAML     |    ConvNet   |   51.67±1.81   |   70.30±1.75   |
|    ProtoNet   |    ConvNet   |   53.34±0.89   |   72.69±0.74   |
|  RelationNet  |    ConvNet   |   54.48±0.93   |   71.32±0.78   |
|      TPN      |    ConvNet   |   59.91±0.94   |   73.30±0.75   |
|   Edge-label  |    ConvNet   |   63.52±0.52   |   80.24±0.49   |
|    **DPGN**   |  **ConvNet** | **69.43±0.49** | **85.92±0.42** |
|      CTM      |   ResNet18   |   64.78±0.11   |   81.05±0.52   |
|    **DPGN**   | **ResNet18** | **70.46±0.52** | **86.44±0.41** |
|     TapNet    |   ResNet12   |   63.08±0.15   |   80.26±0.12   |
| Meta-Transfer |   ResNet12   |   65.62±1.80   |   80.61±0.90   |
|   MetaOptNet  |   ResNet12   |   65.81±0.74   |   81.75±0.53   |
|   Shot-Free   |   ResNet12   |   66.87±0.43   |   82.64±0.39   |
|    **DPGN**   | **ResNet12** | **72.45±0.51** | **87.24±0.39** |


**CIFAR-FS**:

|    Method   |   backbone   | 5way-1shot     |   5way-5shot   |
|:-----------:|:------------:|----------------|:--------------:|
|   ProtoNet  |    ConvNet   | 51.31±0.91     |   70.77±0.69   |
|     MAML    |    ConvNet   | 55.92±0.95     |   72.09±0.76   |
| MatchingNet |    ConvNet   | 61.16±0.89     |   72.86±0.70   |
| RelationNet |    ConvNet   | 62.45±0.98     |   76.11±0.69   |
|  CloserLook |    ConvNet   | 60.53±0.83     |   79.34±0.61   |
|     DN4     |    ConvNet   | 53.15±0.84     |   81.90±0.60   |
|   **DPGN**  |  **ConvNet** | **76.05±0.51** | **89.08±0.38** |
|     FEAT    |   ResNet12   | 68.87±0.22     |   82.90±0.15   |
|   **DPGN**  | **ResNet12** | **75.71±0.47** | **91.48±0.33** |


**Ominiglot**:

|    Method   |   backbone   |  5way-1shot  |  5way-5shot  |
|:-----------:|:------------:|:------------:|:------------:|
|  MatchingNet|    ConvNet   |   43.56±0.84 |   55.31±0.73 |
|    ProtoNet |    ConvNet   |   49.42±0.78 |   68.20±0.66 |
|      MAML   |    ConvNet   |   48.70±1.84 |   55.31±0.73 |
|      DPGN   |    ConvNet   |   66.01±0.36 |   82.83±0.41 |
