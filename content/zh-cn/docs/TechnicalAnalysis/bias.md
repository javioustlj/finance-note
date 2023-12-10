---
title: "BIAS"
linkTitle: "BIAS"
weight: 4
draft: false
description: >
    技术指标之乖离率介绍
---

## 乖离率 BIAS (Bias Ratio)

### 乖离率是什么？

乖离率的英文是BIAS。

bias 是一个单词 其英文释义是：

the fact that the results of research of an experiment are not accurate because a particular factor has not been considered when collecting the information.

bias 在数学或统计学中也可翻译为偏差。

在对bias这个单词的意义了解之后，我们可能对乖离率这个技术指标的意义有了大致的猜测。

通俗的讲，乖离率（BIAS）指标就是反应当前价格偏离移动平均线（MA）的程度。

乖离率指标建立在移动平均的基础上，是由移动平均演变出来的一种技术指标，它通过研判股价在运作过程中与移动均线的分离、聚合程度来指导买卖操作。

### 乖离率的计算

乖离率反应的是价格与价格平均的偏离程度，其计算公式如下：

$$
BIAS(n) = \frac{P_{close} - MA(n)}{MA(n)} \times 100
$$

式中，$P_{close}$为收盘价；$MA(n)$为参数$n$天的移动平均；

乖离率的参数是移动平均线的参数$n$。$n$首先影响$MA$，然后影响$BIAS$。一般来说，$n$选的越大，允许价格远离MA的程度越大。


### 乖离率的应用

第一，考虑BIAS的取值大小。这是产生BIAS的最初的想法，只要BIAS超过某个数值，就应该感到危险（机会）而考虑抛出（买入）。问题的关键在于如何找到这个分界线。

分界线的选择与两个因素有关：首先，BIAS的参数n天的大小。n越大，分界线相应的也应该越高。其次，具体证券在市场中的活跃程度。证券越活跃，分界线越高。

第二，考虑BIAS与价格的背离。BIAS形成从上到下的两个或多个下降的峰，而此时价格还在继续上升，是抛出的信号。BIAS形成从下到上的两个或多个上升的谷，而此时价格还在继续下跌，是买入的信号。
