## 平台
牛客网

## 语言
python2.7.3

## 作业内容

### 题目描述

输入两个整数序列，第一个序列表示栈的压入顺序，请判断第二个序列是否可能为该栈的弹出顺序。

假设压入栈的所有数字均不相等。例如序列1,2,3,4,5是某栈的压入顺序，序列4,5,3,2,1是该压栈序列对应的一个弹出序列，

但4,3,5,1,2就不可能是该压栈序列的弹出序列。（注意：这两个序列的长度是相等的）


### 题目理解



### 解题思路
1. 如果第一个元素相等，直接都弹出，根本不用压入stack
2. 如果stack的最后一个元素与popV中第一个元素相等，将两个元素都弹出
3. 如果pushV中有数据，压入stack
4. 上面情况都不满足，直接返回false。

### 程序
    # -*- coding:utf-8 -*-
    class Solution:
     
        def IsPopOrder(self, pushV, popV):
            # stack中存入pushV中取出的数据
            stack=[]
            while popV:
                # 如果第一个元素相等，直接都弹出，根本不用压入stack
                if pushV and popV[0]==pushV[0]:
                    popV.pop(0)
                    pushV.pop(0)
                #如果stack的最后一个元素与popV中第一个元素相等，将两个元素都弹出
                elif stack and stack[-1]==popV[0]:
                    stack.pop()
                    popV.pop(0)
                # 如果pushV中有数据，压入stack
                elif pushV:
                    stack.append(pushV.pop(0))
                # 上面情况都不满足，直接返回false。
                else:
                    return False
            return True


### 补充知识点
[数据结构——栈](http://blog.51cto.com/9291927/2063393)