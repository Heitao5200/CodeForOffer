## 平台
牛客网

## 语言
python2.7.3

## 作业内容

### 题目描述

用两个栈来实现一个队列，
完成队列的 Push 和 Pop 操作。
队列中的元素为 int 类型。


### 题目理解

#### 什么是栈？

栈（有时称为 “后进先出栈”）是一个项的有序集合，这种排序原则有时被称为 LIFO（后进先出），
其中添加移除新项总发生在同一端。这一端通常称为 “顶部”。与顶部对应的端称为 “底部”。


#### 什么是队列？

队列是项的有序结合，其中添加新项的一端称为队尾，移除项的一端称为队首。这种排序原则有时被称为 
FIFO（先进先出）当一个元素从队尾进入队列时，一直向队首移动，直到它成为下一个需要移除的元素为止。

push：将元素放进队尾

pop： 将队顶的元素删除，并返回

### 解题思路

定义栈

定义push和pop函数



### 程序
```
# -*- coding:utf-8 -*-
class Solution:
    def __init__(self):
        self.stack1 = []  #定义两个stack，
        self.stack2 = []
    def push(self, node):        
        self.stack1.append(node) #往队列中添加元素，将元素放进队尾
    def pop(self): # 没看懂啊
        
        if len(self.stack2):
            return self.stack2.pop()
        while(self.stack1):
            self.stack2.append(self.stack1.pop())
        return self.stack2.pop()    


```


### 补充知识点
