# Python 数据分析与展示

- Numpy
- Matplotlib
- Pandas

摘要：有损地提取数据特征的过程

- 基本统计（含排序）
- 分布、累计统计
- 数据特征：相关性、周期性等
- 数据挖掘（形成知识）


### Python 语言开发工具选择

常用的Python IDE 工具

文本工具类：

- IDLE
- Notepad++
- Sublime Text
- Vim & Emacs
- Atom
- Komodo Edit

集成工具类：
- PyCharm
- Wing
- PyDev & Eclipse
- Visual Studio
- Anaconda & Spyder
- Canopy

conda

- 一个工具，用于包管理和环境管理。
- 包管理与pip类似，管理Python第三方库。
- 环境管理能够允许用户使用不同版本的Python，并能灵活切换Python版本。

anaconda：一个集合，包括conda、某版本Python、一批第三方库。

IPython

它是一个交互式变成环境，是一个功能强大的交互式shell。适合进行交互式数据可视化和GUI应用开发

技巧1 “？”

在一个变量或者函数后面输入？可以获得该变量或者函数的详细信息。

技巧2 run 命令

%run 用于运行.py 程序。注意：%run在一个空的命名空间执行程序。

技巧3 魔术命令

%magic 显示所有魔术命令
%hist IPython 命令的输入历史
%pdb 异常发生后自动进入调试器
%reset 删除当前命名空间中的全部变量或名称
%who 显示Ipython当前命名空间中已经定义的变量
%time statement 给出代码的执行时间，statement 表示一段代码
%timeit statement 多次执行代码，计算综合平均执行时间


### 数据的维度

- 一维数据： 列表和集合
- 二维数据：列表
- 多维数据：列表
- 高维数据：字典类型或数据表示格式

Json、XML、YAML


## NumPy库入门


NumPy是一个开源的Python科学计算基础库，包含：
- 一个强大的N维数组对象ndarray
- 广播功能函数
- 整合C/C++/Fortran代码的工具
- 线性代数、傅里叶变换、随机数生成等功能

Python已有列表类型，为什么需要一个数组对象(类型)？

- 数组对象可以去掉元素间运算所需的循环，使一维向量更像单个数据
- 设置专门的数组对象，经过优化，可以提升这类应用的运算速度
- 数组对象采用相同的数据类型，有助于节省运算和存储空间

ndarray是一个多维数组对象，由两部分构成：
- 实际的数据
- 描述这些数据的元数据（数据维度、数据类型等）

ndarray数组一般要求所有元素类型相同（同质），数组下标从0开始


轴（axis）：保存数据的维度
秩（rank）：轴的数量

.ndim 秩，即轴的数量或维度的数量
.shape ndarray对象的尺度，对于矩阵，n行m列
.size ndarray对象元素的个数，相当于.shape中n*m的值
.dtype ndarray对象的元素类型
.itemsize ndarray对象中每个元素的大小，以字节为单位


ndarray数组的创建方法
