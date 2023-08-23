---
title: 'Leetcode Notes'
date: 2023-08-19  
permalink: /posts/2023/08/leetcode-note/
tags:
  - leetcode
---

### 数组与双指针技巧

**双指针方法**：
1. **左右双指针**：通常用于排序数组，如二分查找。可以将数组分为左半和右半，或用于查找满足条件的两个元素，例如在有序数组中查找两个数的和等于目标值。
2. **快慢指针**：常用于链表，例如寻找链表中的中间节点或判断链表是否有环。
3. **滑动窗口**：主要用于连续数组或字符串的问题，如找出数组中的连续子数组满足某种条件。

**模拟题：旋转矩阵**

**描述**：给定一个数字n，创建一个n x n的二维矩阵，填充从1到n^2的数字，以螺旋的形式。

**步骤**：

1. **初始化矩阵**：创建一个n x n的二维矩阵，并将所有元素初始化为0。

2. **定义边界和计数器**：设定上下左右四个边界，以及一个计数器从1开始。

3. **填充螺旋层**：按照以下顺序填充，直到计数器>n^2：
   a. 从左到右填充顶行，并将上边界下移一位。
   b. 从上到下填充右侧列，并将右边界左移一位。
   c. 从右到左填充底行，并将下边界上移一位。
   d. 从下到上填充左侧列，并将左边界右移一位。

4. **返回结果**：完成所有螺旋层的填充后，返回矩阵。

**示例代码**：

```python
class Solution:
    def generateMatrix(self, n: int) -> List[List[int]]:
        nums = [[0] * n for _ in range(n)]
        count = 1 # 用于记录当前填充的数字

        # 外层循环，每次循环填充一层螺旋
        for layer in range(n // 2): 
            # 定义本层螺旋的边界
            start = layer
            end = n - layer - 1
            
            # 从左至右填充顶行
            for i in range(start, end):
                nums[start][i] = count
                count += 1
            
            # 从上至下填充右列
            for i in range(start, end):
                nums[i][end] = count
                count += 1
            
            # 从右至左填充底行
            for i in range(end, start, -1):
                nums[end][i] = count
                count += 1
            
            # 从下至上填充左列
            for i in range(end, start, -1):
                nums[i][start] = count
                count += 1

        # 如果n为奇数，填充中心点
        if n % 2 != 0:
            nums[n // 2][n // 2] = count
        
        return nums
```
