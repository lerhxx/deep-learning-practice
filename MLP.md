# 多层感知机 Multilayer Perceptron

在输出层和输入层之间增加一个或多个全连接隐藏层，并通过激活函数转换隐藏层的输出。

## 常用的激活函数

- ReLu函数（修正线性单元，Rectified linear unit）
- sigmod 函数（挤压函数，squashing function）
- tanh 函数（双曲正切函数）

### ReLu

最受欢迎，因为实现简单，在各种预测任务中表现良好。

通过将相应的活性值设为0，仅保留正元素，并丢弃所有负元素，激活函数是分段性的。

ReLu 减轻了困扰以往神经网络的提督消失问题。

变体之一：参数化ReLu（Parameterized ReLu, pReLu）

ReLu(x) = max(x, 0)

### sigmod 函数

将范围(-inf, inf)中的任意输入压缩到空间(0, 1)中的某个值

sigmod(x) = 1 / (1 + exp(-x))

当想要将输出视为二元分类问题的概率时，sigmod 仍被广泛作用输出单元上的激活函数

导数：(d/dx)sigmod(x) = exp(-x) / (1+exp(-x))平方 = sigmod(x)(1 - sigmod(x))

### tanh函数

与 sigmod 函数类似，能将其输入压缩转换到区间(-1, 1)上

tanh = (1 - exp(-2x)) / (1 + exp(-2x))

导数；(d / dx)tanh(x) = 1 - tanh平方(x)