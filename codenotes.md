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

## 1.02

### 数组

1. 数组元素插入

某个特定位置：

```python
arr.insert(index, value)
```

尾部：

```python
arr.append(value)
```

2. 数组元素删除

   1. 按索引删除：

   ```python
   del arr[index] #值不返回

   # or

   arr.pop(index)# 值返回
   ```

   2. 按值删除：

   ```python
   arr.remove(value)
   ```

3. 利用切片进行列表逆序排列

```python
arr[::-1]

```

例如，如果转置后的矩阵是 [(1, 4), (2, 5), (3, 6)]，那么 [::-1] 操作后就变成了 [(3, 6), (2, 5), (1, 4)]。

4. 矩阵的转置

```python
zip(*matrix)
```

5. 注意区别

```python
nums = nums[len(nums) - k:] + nums[:len(nums) - k]
nums[:] = nums[len(nums) - k:] + nums[:len(nums) - k]
```

- 这种写法并没有直接修改原始列表 nums，而是创建了一个新的列表，并将其赋值给了 nums 变量。原始列表 nums 的内容保持不变。
- 尽管 **nums**变量指向了一个新的列表对象，但是如果有**其他变量**也指向了原始列表 **nums**，那么这些变量不会受到新列表的影响

- 使用 **nums[:]** 来选择整个列表，这意味着将右侧的切片结果替换掉整个列表

类似于列表的深复制和浅复制：

```python
import copy
A = nums[:]  # 深复制
B = nums     # 浅复制
deep_copy = copy.deepcopy(nums)# 深复制
```

- 深复制：创建一个新的列表对象，并将原列表的所有元素都复制到新列表中
- 浅复制：创建一个新的列表对象，但是新列表的元素是原列表的引用，因此如果原列表中的元素发生变化，新列表也会跟着变化
