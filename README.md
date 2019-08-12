# Instance Enhancement Batch Normalization: an Adaptive Regulator of Batch Noise
[![996.ICU](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu) 
![GitHub](https://img.shields.io/github/license/gbup-group/DIANet.svg)
![GitHub](https://img.shields.io/badge/gbup-%E7%A8%B3%E4%BD%8F-blue.svg)

By [Senwei Liang*](https://leungsamwai.github.io), [Zhongzhan Huang*](https://github.com/dedekinds) (* contribute equally), [Mingfu Liang](https://github.com/wuyujack) and [Haizhao Yang](https://haizhaoyang.github.io/).

This repository is the implementation of "Instance Enhancement Batch Normalization: an Adaptive Regulator of Batch Noise" [[paper]](https://arxiv.org)  on CIFAR-100 dataset.

## Introduction
Instance En-hancement Batch Normalization (IEBN) is an attention-based version of BN which recalibrates channel information of BN by a simple linear transformation.

## Requirement
* Python 3.6 and [PyTorch 1.0](http://pytorch.org/)

## Usage
  ```
python cifar.py -a iebn_resnet --dataset cifar100 --block-name bottleneck --depth 164 --epochs 164 --schedule 81 122 --gamma 0.1 --wd 1e-4 --checkpoint checkpoints/cifar100/resnet-164-iebn
  ```

## Results
|                 | original |  IEBN  |
|:---------------:|:--------:|:------:|
|    ResNet164    |   74.29  |  77.09 |


**Notes:**
- Testing on **2*GPU**

## Citing IEBN

## Acknowledgments
Many thanks to [bearpaw](https://github.com/bearpaw) for his simple and clean [Pytorch framework](https://github.com/bearpaw/pytorch-classification) for image classification task.
