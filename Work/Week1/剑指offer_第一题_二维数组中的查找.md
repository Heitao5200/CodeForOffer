## 平台
牛客网

## 语言
python2.7.3

## 作业内容

### 题目描述
    在一个二维数组中（每个一维数组的长度相同），
    每一行都按照从左到右递增的顺序排序，
    每一列都按照从上到下递增的顺序排序。
    请完成一个函数，输入这样的一个二维数组和一个整数，
    判断数组中是否含有该整数。

### 题目理解

#### 什么是二维数组
python里面没有数组的概念，而是列表(List),即二维列表相当于二维数组 。
python里面的二维数组，主要有list和numpy.array两种。其实还有matrices（必须是2维的），
numpy arrays (ndarrays) 可以是多维的。
[list和numpy.array的区别](https://blog.csdn.net/qq_30490125/article/details/51445390)


### 解题思路
此题是判断数组中是否存在某个元素
可以用[target in array[j]](https://blog.csdn.net/qzc70919700/article/details/72983513)
对这个二维数组里面的每个一维数组遍历，判断是否存该元素

### 程序
    # -*- coding:utf-8 -*-
    class Solution:
        def Find(self, target, array):
            # write code here
            rows = len(array) - 1  # 二维数组里的一维数组的个数
            i = rows
            j = 0
            while j <= i:
                result = target in array[j] #判断是否存该元素
                j += 1
                if result == True:   # 存在则返回  不存在则继续循环 最终返回False
                    return True
            return False

### 补充知识点

python中的数组

[Python语法：数组](https://blog.csdn.net/qzc70919700/article/details/72983513)
