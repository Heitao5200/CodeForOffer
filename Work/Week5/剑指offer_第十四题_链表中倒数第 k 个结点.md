
## 平台
牛客网

## 语言
python2.7.3

## 作业内容

### 题目描述
输入一个链表，输出该链表中倒数第k个结点。



### 题目理解

### 解题思路
* 确定链表的节点个数lenth
* 输入0 < k <节点个数
* [翻转链表](剑指offer_第十五题_反转链表.md)
* 遍历链表前length-k个 输出最后一个


### 程序
    
    class Solution:
        def FindKthToTail(self, head, k):
            if head==None or k<=0:
                return None
            length = 1
            node = head
            while node.next!=None:
                length+=1
                node = node.next
            if k>length:
                return None
            for i in range(length-k):
                head = head.next
            return head




### 补充知识点

[python数据结构之链表（一）](https://www.cnblogs.com/king-ding/p/pythonchaintable.html)


























