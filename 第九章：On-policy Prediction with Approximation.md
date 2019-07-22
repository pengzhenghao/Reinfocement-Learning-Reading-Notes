# 第九章：On-policy Prediction with Approximation

彭正皓



## 本书第二部分前言

现在进入本书第二部分。相比起第一部分表格法，现在的问题是：

* 任意大的State空间
* State几乎不可能精确的重现，因此需要**泛化性**。
* 泛化性其实就是**函数近似问题**。这是有监督学习。

* 强化学习相比有监督有一些不同。
  * 不稳定性
  * bootstrapping
  * delayed targets
  * 等等
* 这些问题将会在第9章到第12章解答。



## 第九章前言

* On-Policy 指的是用一个已知的策略来获得经验，以近似一个价值函数$v_\pi$。
* 通常用参数化的函数来作为近似器。$\hat{v}(s, w) \approx v_\pi(s)$
  * 一个参数的变动会影响很多不同的state的结果。利用一个state来更新参数，就会影响许多个state。泛化性由此产生。
* 如今算法可以用于Partially Observable Problems。



## 9.1 Value-function Approximation

* 本书提到的所谓“Prediction Methods”，都可以概括为给定一个state，给出一个output罢了。
* 因此可以使用各式各样的函数近似算法。
* 然而不是所有的算法都好。因为：
  1. 学习可能是online的。因此近似算法必须能够处理增量的学习样本。（样本会变来变去）
  2. 目标函数是nonstationary的。（policy会变来变去，从而影响value function的“精确值”。）



## 9.2 The Prediction Objective ($\overline{VE}$)

本节的目的是寻找一个“**预测目标**”。











