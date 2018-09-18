## 平台
牛客网

## 语言
python2.7.3

## 作业内容

### 题目描述
把一个数组最开始的若干个元素搬到数组的末尾，我们称之为数组的旋转。
输入一个非减排序的数组的一个旋转，输出旋转数组的最小元素。
如数组 {3,4,5,1,2} 为{1,2,3,4,5}的一个旋转，该数组的最小值为 1。
NOTE：给出的所有元素都大于 0，若数组大小为 0，请返回 0。

### 题目理解

[什么是数组？](https://blog.csdn.net/liushut/article/details/77994978)

非递减排序:就是从小到大或者允许中间有相等的情形

### 解题思路

找出数组的最小元素
在所给数组从最小值前切分
调换位置

### 程序(还需理解)

```
# -*- coding:utf-8 -*-
class Solution:
    def minNumberInRotateArray(self, rotateArray):
        # write code here
        if rotateArray == []:
            return 0
        _len = len(rotateArray)
        left = 0
        right = _len - 1
        while left <= right:
            mid = int((left + right) >> 1)
            if rotateArray[mid]<rotateArray[mid-1]:
                return rotateArray[mid]
            if rotateArray[mid] >= rotateArray[right]:
                # 说明在【mid，right】之间
                left = mid + 1
            else:
                # 说明在【left，mid】之间
                right = mid - 1
        return rotateArray[mid]

```


### 补充知识点
