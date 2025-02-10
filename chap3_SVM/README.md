# 支持向量机 (SVM)

## 问题描述

本次作业分为三个部分.

1. 使用基于某种核函数 (线性、多项式或高斯核函数) 的 SVM 解决非线性可分的二分类问题, 数据集为 `train_kernel.txt` 及 `test_kernel.txt`.
2. 分别使用线性分类器 (squared error)、logistic 回归 (cross entropy error) 以及 SVM (hinge error) 解决线性二分类问题, 并比较三种模型的效果, 数据集为 `train_linear.txt` 及 `test_linear.txt`. 

   > 三种误差函数定义如下 (Bishop P327):
   >
   > $$
   > E _{linear}=\sum\limits_{n=1}^N\,(y _n-t _n)^2+\lambda\big\|\mathbf{w}\big\|^2
   > $$
   >
   > $$
   > E _{logistic}=\sum\limits _{n=1}^N\,\log(1+\exp(-y _nt _n))+\lambda\big\|\mathbf{w}\big\|^2
   > $$
   >
   > $$
   > E _{SV\!M}=\sum\limits _{n=1}^N\,[1-y _nt _n]+\lambda\big\|\mathbf{w}\big\|^2
   > $$
   >
   > 其中 $y _n=\mathbf{w}^Tx _n+b$ 为类别标签.
   >
3. 使用多分类 SVM 解决三分类问题, 数据集为 `train_multi.txt` 及 `test_multi.txt`. (5%)

## 数据集

MNIST 数据集包括 60000 张训练图片和 10000 张测试图片. 图片样本的数量已经足够训练一个很复杂的模型 (例如 CNN 的深层神经网络). 它经常被用来作为一个新的模式识别模型的测试用例, 而且它也是一个方便学生和研究者们执行用例的数据集. 除此之外，MNIST 数据集是一个相对较小的数据集, 可以在你的笔记本 CPUs 上面直接执行.

## 题目要求

- [ ] 请使用代码模板 `rbm.py`, 补全缺失部分, 尽量不改动主体部分.
- [ ] 推荐使用 python 及 numpy 编写主要逻辑代码, 适度使用框架.
