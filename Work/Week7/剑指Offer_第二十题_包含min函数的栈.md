## 平台
牛客网

## 语言
python2.7.3

## 作业内容

### 题目描述
定义栈的数据结构，请在该类型中实现一个能够得到栈中所含最小元素的min函数（时间复杂度应为O（1））。



### 题目理解
1. 由于题目要求的是一个栈，所以想要通过栈内元素进行排序，这个是不可行的。
2. 由于存在每次的push和pop操作。所以，通过在入口设置最小值，然后不断更新最小值的方式也是不可取的。因为，pop一次之后就失效了。



### 解题思路

1. 创建数据栈和辅助栈表
2. 往空的数据栈里压入元素，是最小值的话，也将其压入辅助栈
3. 接下来再往数据栈中压入下一个元素，是最小值的话，同时将其压入数据栈和辅助栈，若不是最小值，则只压入数据栈。
4. 数据栈和最小栈同时弹出


### 程序
    # -*- coding:utf-8 -*-
    class Solution:
        def __init__(self):
            self.stack = []
            self.assist = []
             
        def push(self, node):
            min = self.min()
            if not min or node < min:
                self.assist.append(node)
            else:
                self.assist.append(min)
            self.stack.append(node)
             
        def pop(self):
            if self.stack:
                self.assist.pop()
                return self.stack.pop()
         
        def top(self):
            # write code here
            if self.stack:
                return self.stack[-1]
             
        def min(self):
            # write code here
            if self.assist:
                return self.assist[-1]



### 补充知识点
