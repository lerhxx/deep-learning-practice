### [Pytorch｜标量、向量、张量的区别](https://www.cnblogs.com/zhangxuegold/p/17517066.html)

### 基本概念

- 标量(Scalar)：是一个单独的数，没有方向和大小
- 向量(Vector)：一个有方向和大小的量
- 张量(Tensor)：一个多维数组，它可以包含多个向量和标量。向量可以看作是一维张量，矩阵可以看作是二维张量

- 因变量y：预测的目标，称为标签(label)或目标(target)
- 自变量x：特征(feature)或协变量(covariate)

- 矢量化：通常指对数据中单个元素执行的操作转换为可同时应用于整个数组或矩阵的操作的过程
- 超参数：可以调整但不再训练过程中更新的参数，如批量大小和学习率的值
- 调参：选择超参数的过程

标量、向量和张量是三个不同的数学概念，它们描述了不同纬度的不同性质的数值和物理量。

### 向量和张量的维度概念

- 向量中，维度指向量的长度或分量的个数，也就是向量的维数。
- 张量中，维度指张量的秩或阶数，也就是张量所包含的轴数或维数。


### 运算

- Hadamard 积(Hadamard product)：两个矩阵按元素的乘法
- 点积(dot product)：两个向量相同位置的按元素乘积的和
- 矩阵-向量积(matrix-vector product)：矩阵和向量的乘法，得到一个长度为m的列向量

### 仿射变换

两种简单的变换：线性变换、平移变换。

包括：缩放 Scale、平移 Treansform、旋转 Rotate、反射 reflectipn（镜像）、错切 Shear mapping（倒影）

仿射变换保持不变的性质：

- 凸性
- 共线性：若几个点变换钱在一条线上，则变换后仍在一条线上
- 平行性：变换前平行，变换后仍平行
- 共线比例不变性：变换钱一条线上两条线段比例，变换后比例不变

### 特征缩放

让梯度下降得更快

方法：

- 除以最大值
- Mean normalization：(x-μ)/(max-min)
- Z-score normalization：(x-μ)/σ

### 广播极致

1、通过适当复制元素来扩展一个或两个数组，以便在转换之后，两个张量具有相同的形状
2、对生成的数组执行按元素操作

### 全连接层(fully-connected layer)或稠密层(dense layer)

每个输入都与每个输出相连

通常位于神经网络的最后几层，用于分类任务的输出层