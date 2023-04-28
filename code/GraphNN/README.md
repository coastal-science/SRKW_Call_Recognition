# DPGN: Distribution Propagation Graph Network for Few-shot Learning

Implementation of [DPGN: Distribution Propagation Graph Network for Few-shot Learning](https://arxiv.org/abs/2003.14247). 

<p align='center'>
  <img src='figure/dpgn.png' width="800px">
</p>

## Requirements

CUDA Version: 10.1

Python : 3.6

To install dependencies:

```setup
sudo pip3 install -r requirements.txt
```
## Dataset

The dataset directory should look like this:
```bash
├── dataset
    ├── mini-imagenet
        ├── mini_imagenet_test.pickle   
        ├── mini_imagenet_train.pickle  
        ├── mini_imagenet_val.pickle
    ├── cifar-fs
        ├── cifar_fs_test.pickle   
        ├── cifar_fs_train.pickle  
        ├── cifar_fs_val.pickle
    ├── cub-200-2011
        ├── attributes   
        ├── bounding_boxes.txt 
        ├── classes.txt
        ├── image   
        ├── image_class_labels.txt 
        ├── images
        ├── images.txt   
        ├── parts
        ├── README
        ├── split
        ├── train_test_split.txt
	├── omniglot
        ├── images_background   
        ├── cifar_fs_train.pickle  
        ├── cifar_fs_val.pickle
```

## Training

To train the model(s) in the paper, run:

```train
python3 main.py --dataset_root dataset --config config/5way_1shot_resnet12_mini-imagenet.py --num_gpu 1 --mode train
```


## Evaluation

To evaluate the model(s) in the paper, run:

```eval
python3 main.py --dataset_root dataset --config config/5way_1shot_resnet12_mini-imagenet.py --num_gpu 1 --mode eval
```

## Pre-trained Models
<!--[**best_checkpoints**](best_checkpoints) directory contains pre-trained model under settings of 5way-1shot and 5way-5shots for mini-ImageNet dataset with ResNet12 backbone.-->
[This Google Drive](https://drive.google.com/open?id=1ZF4wB4tId7YZX6m_HYdo87f_Q1RjaiYN) contains pre-trained model under settings of 5way-1shot and 5way-5shots for mini-ImageNet dataset with ResNet12 backbone.

## Results
```bash
# Default checkpoints directory is:
./checkpoints
```

```bash
# Default logs directory is:
./logs
```