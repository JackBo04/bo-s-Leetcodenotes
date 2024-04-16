# 刷题笔记

## 1.01

### 数组

1. 新建一个数组，并初始化为 0。

```python
arr = [0] * n
arr = [0 for i in range(n)]
```

2. 复制一个数组

```python
arr1 = [1, 2, 3]
arr = arr1 + arr1
```

### 矩阵

1. 矩阵行数

```python
m = len(matrix)
```

2. 矩阵列数

```python
n = len(matrix[0])
```

3. 矩阵行求和
   使用了列表推导式，目的是计算矩阵中每行的和，并将结果存储在列表 row_sum 中。

```python
row_sum = [sum(matrix[i]) for i in range(m)]
```

4. 矩阵列求和

```python
col_sum = [sum(matrix[i][j] for i in range(m)) for j in range(n)]
```
