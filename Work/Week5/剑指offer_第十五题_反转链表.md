## 平台
牛客网

## 语言
python2.7.3

## 作业内容

### 题目描述
输入一个链表，反转链表后，输出新链表的表头。



### 题目理解



### 解题思路
* 判断链表长度是否大于1或这为空

假设当前链表的头节点为head  当前节点为now 
步骤一：将now的next指针指向head
步骤二：将反转后的now节点设置为反转部分新的head
步骤三：步骤一之前应该将now的下一个节点保存下来，在进行步骤三



### 程序

    class Solution:
        def ReverseList(self, pHead):
            if not pHead:
                return pHead
            p=pHead
            q=p.next
            p.next=None
            while q:
                r=q.next
                q.next=p
                p=q
                q=r
            return p

### 补充知识点
[链表](https://pan.baidu.com/s/1t1TPdex59ipd0lj7jxkIGA)