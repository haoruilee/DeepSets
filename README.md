# DeepSets

Code and models for the paper [Deep Sets](https://papers.nips.cc/paper/6931-deep-sets)



===

# 摘要
这篇论文研究重点是处理集合类型数据的机器学习任务的建模问题。传统的任务中往往只考虑如何操作定长的向量，而对于集合数据，我们需要考虑如何处理它的“排列不变性”（invariant to permutations）。如何处理集合的这个问题广泛存在，比如：总体参数估计[3]、堤坝压力计数据的异常检测[4]、宇宙学[5,6]。本文提出一些基本定理用于描述排列不变函数，并提出所有排列不变目标函数必须归属于的函数族。这个函数族有特殊的结构能让我们设计深度模型处理集合数据并且应用在包括无监督学习任务和有监督学习任务这些场景中。我们也推导了深度模型中“排列恒等”（permutation equivariance）的充分必要条件。最后，我们的方法被应用在总体参数估计、点云分类、集合扩展和异常检测任务中，展示了高可应用性的能力.

# 贡献点

提出一个通用的框架去处理集合输入——DeepSets，并且展示这个结构的特征对于排列不变来说是充分必要的。我们扩展了该架构，以允许对任意对象进行条件处理基于此架构，我们开发了一个深度网络，可以在大小可能不同的集合上运行我们展示了一种简单的参数共享方案可以对有监督和半监督场景中的集合进行一般处理最后，我们通过对各种问题的实验证明了我们框架的广泛适用性


08 NIPS 2017《Deep Sets》论文翻译与阅读笔记 - goldfish的文章 - 知乎
https://zhuanlan.zhihu.com/p/368357090

===


We study the problem of designing models for machine learning tasks defined on sets. In contrast to the traditional approach of operating on fixed dimensional vectors, we consider objective functions defined on sets and are invariant to permutations. Such problems are widespread, ranging from the estimation of population statistics, to anomaly detection in piezometer data of embankment dams, to cosmology. Our main theorem characterizes the permutation invariant objective functions and provides a family of functions to which any permutation invariant objective function must belong. This family of functions has a special structure which enables us to design a deep network architecture that can operate on sets and which can be deployed on a variety of scenarios including both unsupervised and supervised learning tasks. We demonstrate the applicability of our method on population statistic estimation, point cloud classification, set expansion, and outlier detection.

## Code Structure

Here we provide code to replicate some of the experiments reported in the paper. Please look at `README` for individual experiments.

```
/
├── DigitSum: Sum of Set of Digits (Text/Image)
│   
├── PointClouds: Classification of Point Cloud Data
│   
├── PopStats: Estimation population statistics from iid sample set of data
│   
├── SetExpansion: For expanding a given set from a large pool of candidates
```

## Citation
If you use this code, please cite our paper
```
@incollection{deepsets,
title = {Deep Sets},
author = {Zaheer, Manzil and Kottur, Satwik and Ravanbakhsh, Siamak and Poczos, Barnabas and Salakhutdinov, Ruslan R and Smola, Alexander J},
booktitle = {Advances in Neural Information Processing Systems 30},
editor = {I. Guyon and U. V. Luxburg and S. Bengio and H. Wallach and R. Fergus and S. Vishwanathan and R. Garnett},
pages = {3391--3401},
year = {2017},
publisher = {Curran Associates, Inc.},
url = {http://papers.nips.cc/paper/6931-deep-sets.pdf}
}
```
