# 深度学习相关模块
## tensorflow
tensorflow相关笔记
## LeastSquareMethod
最小二乘法
## LUDecomposition
LU矩阵分解

# 概念
## 超定方程
对于方程组Ax=b，A为n×m矩阵，如果A列满秩，且n>m，则方程组没有精确解，此时称方程组为超定方程组。
## 超定方程解法
在视觉标定中经常碰到这三种超定方程，简单总结下它们的一般解法。
### 线性非齐次方程组
Ax=b，b~=0：最小二乘法  在matlab中  可以直接x=A\b，自己一般习惯x=(A'*A)\(A*b)，两者在matlab中处理方法是一样的即   最小二乘法。
### 线性齐次方程组
Ax=0：一般用svd分解，后者是求解特征后，得到最小的特征值对应的特征向量为方程组的解，解会有很多组，可以选取归一化的那组。当然方程组一般是超定的，应该应经过A'*A处理。
### 非线性方程组
levenlerg-marquaerdt，牛顿法等，前者用得比较多，在matlab中用lsqnonlin函数进行求救

## 矩阵性质
正交矩阵的逆=正交矩阵的转置

