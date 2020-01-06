## PyTorch implementation of  [\[1611.06440 Pruning Convolutional Neural Networks for Resource Efficient Inference\]](https://arxiv.org/abs/1611.06440) ##

This demonstrates pruning a VGG16 based classifier that classifies a small dog/cat dataset.


This was able to reduce the CPU runtime by x3 and the model size by x4.


At each pruning step 512 filters are removed from the network.


Usage
-----

This repository uses the PyTorch ImageFolder loader, so it assumes that the images are in a different directory for each category.

Train

......... dogs

......... cats


Test


......... dogs

......... cats


The images were taken from [here](https://www.kaggle.com/c/dogs-vs-cats) but you should try training this on your own data and see if it works!

Training:
`python finetune.py --train`

Pruning:
`python finetune.py --prune`
