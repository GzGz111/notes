# Numpy
用法
```python
import numpy as np
```
## 数组基础
### 同化
#### 整数型
插入浮点数，被截断，数组仍然为整数型
```python
arr1 = np.array([1,2,3])
arr1[0]=100.9
print(arr1)
```
result:
```
[100 2 3]
```
#### 浮点型
插入整数型，被升级，数组仍然为浮点型
```python
arr2 = np.array[1.0,2,3]
arr2[1] = 10
print(arr2)
```
result:
```
[1. 10. 3.]
```
## astype()
```python
arr2 = arr1.astype(float)
print(arr2)
```
result:
```
[1. 2. 3.]
```
或
```python
arr3 = arr2.astype(int)
print(arr3)
```
result:
```
[1 2 3]
```
## 运算变化
```python
arr = np.array([1,2,3])
print(arr)
```
result:
```
[1 2 3]
```
### 整数行与浮点型运算
```python
print(arr + 0.0)
print(arr * 1.0)
```
result:
```
[1. 2. 3.]
[1. 2. 3.]
```
### 整数型与除法
```python
print(arr / 1)
```
result:
```
[1. 2. 3.]
```
### 整数型数组与浮点型数组运算
```python
int_arr=np.array[1,2,3]
float_arr=np.array[1.0,2,3]
print(int_arr + float_arr)
```
result:
```
[2. 4. 6.]
```
## 数组维度
一维数组用一层中括号表示，形状参数为：x 或 (x,)。如\[1,2,3]形状参数为 3 或 (3,)
二维数组用两层中括号表示，形状参数为：(x,y)。如\[\[1,2,3]]形状参数为 (1,3)
三维数组用三层中括号表示，形状参数为：(x,y,z)。如\[\[\[1,2,3]]]形状参数为 (1,1,3)
### np.ones()与shape
传入形状造出数组
```python
import numpy as np
arr3 = np.ones((1,1,3))
print(arr3)
print(arr3.shape)
```
result:
```
[[[1. 1. 1.]]]
(1,1,3)
```
### 维度转换
reshape
#### 创建二维
```python
arr2=np.arrange(10).reshape(2,5)
print(arr2)
```
result:
```
[[0 1 2 3 4]
[5 6 7 8 9]]
```
#### 降级为一维
```python
arr1 = arr2.reshape(-1)
print(arr1)
```
result:
```
[0 1 2 3 4 5 6 7 8 9]
```
## 数组创建
### 种类
#### 向量
```python
arr1 = np.array([1,2,3])
print(arr1)
```
result:
```
[1 2 3]
```
#### 行矩阵
```python
arr2 = np.array([1,2,3])
print(arr2)
```
result:
```
[[1 2 3]]
```
#### 列矩阵
```python
arr3 = np.array([1],[2],[3])
print(arr3)
```
result:
```
[[1]
 [2]
 [3]]
```
### 递增数组
arrange参照python
arrange(1,21,2)从1开始到21之前结束，步长为2
```python
arr3 = np.arrange(1,21,2)
print(arr3)
```
result:
```
[1 3 5 7 9 11 13 15 17 19]
```
### 同值数组
#### 全0数组
```python
arr1 = np.zeros((1,3))
print(arr1)
```
result:
```
[[0. 0. 0.]]
```
#### 全1 数组
```python
arr2 = np.ones(3)
```
result:
```
[1. 1. 1.]
```
#### 全3.14数组
```python
arr3 = 3.14 * np.ones((2,3))
print(arr3)
```
result:
```
[[3.14 3.14 3.14]
[3.14 3.14 3.14]]
```
### 随机数组
np.random
#### 0-1均匀分布的浮点型随机数组
形状为5的向量
```python
arr1 = np.random(5)
print(arr1)
```
#### 整数型随机数组
10到100的(1,15)矩阵
```python
arr2 = np.random.randint(10,100,(1,15))
print(arr2)
```
#### 正太分布的随机数组
0到1正太分布形状为(2,3)的矩阵
```python
arr3 = np.random.normal(0,1,(2,3))
print(arr3)
```