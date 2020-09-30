# Instance Enhancement Batch Normalization: an Adaptive Regulator of Batch Noise
[![996.ICU](https://img.shields.io/badge/link-996.icu-red.svg)](https://996.icu) 
![GitHub](https://img.shields.io/github/license/gbup-group/DIANet.svg)
![GitHub](https://img.shields.io/badge/gbup-%E7%A8%B3%E4%BD%8F-blue.svg)

By [Senwei Liang*](https://leungsamwai.github.io), [Zhongzhan Huang*](https://github.com/dedekinds) (* contribute equally), [Mingfu Liang](https://github.com/wuyujack) and [Haizhao Yang](https://haizhaoyang.github.io/).

This repository is the implementation of "Instance Enhancement Batch Normalization: an Adaptive Regulator of Batch Noise" [[paper]](https://arxiv.org/abs/1908.04008)  on CIFAR-100 dataset. Our paper has been accepted for presentation at the Thirty-Fourth AAAI Conference on Artificial Intelligence (AAAI-20). You can also check with the [AAAI proceeding version](https://aaai.org/ojs/index.php/AAAI/article/view/5917).

## Introduction
Instance Enhancement Batch Normalization (IEBN) is an attention-based version of BN which recalibrates channel information of BN by a simple linear transformation.

<p align="center">
  <img src="https://github.com/gbup-group/IEBN/blob/master/figures/iebn.jpg" width="400" height="300">
</p>

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
- Training on 2 GPUs

## Citing IEBN

```
@inproceedings{liang2020instance,
  title={Instance Enhancement Batch Normalization: An Adaptive Regulator of Batch Noise.},
  author={Liang, Senwei and Huang, Zhongzhan and Liang, Mingfu and Yang, Haizhao},
  booktitle={AAAI},
  pages={4819--4827},
  year={2020}
}
```

## Acknowledgments
Many thanks to [bearpaw](https://github.com/bearpaw) for his simple and clean [Pytorch framework](https://github.com/bearpaw/pytorch-classification) for image classification task.
