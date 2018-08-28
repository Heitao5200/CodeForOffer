## 平台
牛客网

## 语言
python2.7.3

## 作业内容

### 题目描述
输入一个链表，按链表值从尾到头的顺序返回一个ArrayList。

### 题目理解
什么是链表
链表的操作有哪些


### 解题思路
输入一个链表
倒序

### 程序
    class Solution:
        def printListFromTailToHead(self, listNode):
            ret = [] #定义空列表
            head = listNode
            while(head):
                ret.append(head.val) #将值添加到列表
                head = head.next
            ret.reverse()
            return ret

### 补充知识点
[python 数据结构之链表（一）](https://www.cnblogs.com/king-ding/p/pythonchaintable.html)