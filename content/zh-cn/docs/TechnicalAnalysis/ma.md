---
title: "MA"
linkTitle: "MA"
weight: 2
draft: false
description: >
    技术分析中的技术指标相关知识介绍
---

## 移动平均线  MA (Moving Average)

### MA的计算

$$
MA(n) = \frac{n天的价格相加}{n}
$$

MA就是连续若干天的价格的算数平均。天数通常选为5日（一周），10日（两周），20日（一月），60日（三月），120日（半年），250日（一年）等

### MA的特性和作用

1. 追踪趋势。MA能够表示价格的趋势，不受小的反向波动影响，并追随这个趋势。原始数据得到的价格图标不是很容易看出这个趋势。
2. 滞后性和稳定性。由于MA是由多天的价格的平均，所以一天的变动对MA的影响就没那么大，所以MA的值相对证券价格来说比较稳定不会被暂时的小的波动所迷惑，但同时，它反应趋势变化也会滞后于趋势本身。
3. 助涨助跌性和支撑压力性。当价格突破了MA时，无论是向上突破还是向下突破，价格都有继续沿着该方向继续的惯性，这就是MA的助涨助跌性。浙使得MA具有了一定的支撑线和压力线的特性。MA被突破，也可以认为支撑性和压力线被突破。

### MA的应用

使用MA的经典方法时格兰维尔（Granville）法则，

买入信号

1. 平均线从下降开始走平，价格从下向上穿过平均线；
2. 价格连续上升远离平均线，突然下降，但在平均线附近再度上升；
3. 价格跌破平均线并连续暴跌。（个人不同意这一点，可以更多考虑乖离率指标）

卖出信号

1. 平均线从上升开始走平，价格从上向下穿过平均线；
2. 价格连续下降远离平均线，突然上升，但在平均线附近再度下跌；
3. 价格上穿平均线并连续暴涨。（这一点很难同意，可以更多考虑乖离率指标）

值得注意的是，在趋势形成后的中途修正阶段或局部反弹和回档，MA的信号出现的很频繁，会发生很多错误的信号。

## 平滑异同移动平均线 MACD(Moving Average Convergence and Divergence)

- MACD (Moving Average Converagence and Divergence) 平滑异同移动平均线
- DIF (Difference) 正负差
- DEA (Difference exponential average) 异同平均数
- EMA (Exponential Moving Average) 指数移动平均线

## MACD 的计算

MACD的计算比较复杂，它是由DIF和DEA两部分组成，DIF是核心，DEA是辅助。但是MIF和DEA的计算都依赖于EMA.

EMA是 Exponential Moving Average 的缩写，称作指数移动平均线。

EMA公式如下：

$$
EMA(P_{close}, N)_{today} = a \times P_{close} + (1 - a) \times EMA_{yesterday}
$$

其中 $a = \frac{2}{N+1}$, 

设$P_i$ 为每日收盘价，其中 $i = 1, 2, \cdots n$， 默认 $EMA(1) = P_1$

$$
\begin{align}
EMA(1) &= P_1 \notag \\\
EMA(2) &= aP_2 + （1-a)P_1 \notag \\\
EMA(3) &= aP_3 + a(1-a)P_2 + (1-a)^2P_1 \notag \\\
\cdots \notag \\\
EMA(n) &= aP_n + a(1-a)P_{n-1}  + a(1-a)^2P_{n-2} + \cdots + a(1-a)^{n-2}P_2 + (1-a)^{n-1}P_1 \notag 
\end{align}
$$

从上面的公式可以看出，a越大，最新价对EMA的影响就越大；a越小，最新价对EMA的影响就越小。而a是和N成反比的，即N越小，则最新价对EMA的影响就越大；N越大，最新价对EMA的影响就越小。

所以我们可以说 $EMA(P_{close}, 12)$ 比 $EMA(P_{close}, 26)$ 对于最新价格的变化更为的灵敏。


$$
DIF = EMA(P_{close}, 12) - EMA(P_{close}, 26)
$$

$$
DEA = EMA(DIF_{today}, 9)
$$

$$
MACD = BAR = 2 \times (DIF - DEA)
$$

## MACD 各指标的意义

### DIF 意义

1. $DIF > 0$，说明短期指数平滑线比长期指数平滑线高，是多头市场，股票价格处于上涨阶段。
2. $DIF < 0$，说明短期指数平滑线比长期指数平滑线低，是空头市场，股票价格处于下跌阶段。
3. $DIF$ 的绝对值越大表明上涨或下跌的趋势越强烈。

### DEA 意义

DEA 一般不会单独应用，它是DIF的补充，相对来说DEA变化的更缓慢平滑。

1. $DEA > 0$，说明短期指数平滑线比长期指数平滑线高，是多头市场，股票价格处于上涨阶段。
2. $DEA < 0$，说明短期指数平滑线比长期指数平滑线低，是空头市场，股票价格处于下跌阶段。
3. $DEA$ 的绝对值越大表明上涨或下跌的趋势越强烈。

### MACD的意义

1. $MACD > 0$，即DIF上穿DEA，说明DIF趋势变化走强，此时显示为hong
2. $DEA < 0$，说明短期指数平滑线比长期指数平滑线低，是空头市场，股票价格处于下跌阶段。
3. $DEA$ 的绝对值越大表明上涨或下跌的趋势越强烈。

## MACD的应用

1. 考虑DIF和DEA的取值和两者之间的相对取值。$DIF > 0$，说明是多头市场，当DIF 和DEA都是正值时，多头市场的信号更明确。DIF向上突破DEA是买入信号，DIF向下跌破DEA应获利了结。反之，当DIF和DEA均为负值时，属于空头市场。
2. 考虑DIF和DEA曲线的走向。这属于技术指标的背离，具体地说，如果DIF或DEA的走向与价格走向相背离，则是采取行动的信号 ---- 底背离买进，顶背离卖出。


参考：
1. https://zhuanlan.zhihu.com/p/153426634
2. https://zhuanlan.zhihu.com/p/138533574
3. https://zhuanlan.zhihu.com/p/361132689
4. https://zhuanlan.zhihu.com/p/261362694
