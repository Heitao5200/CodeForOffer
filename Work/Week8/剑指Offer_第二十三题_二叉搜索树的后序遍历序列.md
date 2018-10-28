## 平台
牛客网

## 语言
python2.7.3

## 作业内容

### 题目描述
输入一个整数数组，判断该数组是不是某二叉搜索树的后序遍历的结果。

如果是则输出Yes,否则输出No。假设输入的数组的任意两个数字都互不相同。



### 题目理解

### 解题思路
**不是**判断一个给定的数组**是不是**一个（原先）给定的二叉搜索树的对应后序遍历的结果

**而是**判断一个给定的数组**是不是能够对应到一个具体的二叉搜索树的后序遍历结果**

* 左子树都比根节点小，右子树都比根节点大

递归的思想:



### 程序

   class Solution:
       def VerifySquenceOfBST(self, sequence):
           # write code here
           if not sequence:
               return False
           if len(sequence)==1:
               return True
           length=len(sequence)
           root=sequence[-1]
           i=0
           while  sequence[i]<root:
               i=i+1
           k=i
           for j in range(i, length-1):
               if sequence[j] < root:
                   return False
           left_s = sequence[:k]
           right_s = sequence[k:length-1]
             
           leftIs = True
           rightIs = True
             
           if len(left_s) > 0:
               leftIs = self.VerifySquenceOfBST(sequence=left_s)
           if len(right_s) > 0:
               rightIs = self.VerifySquenceOfBST(sequence=right_s)
    
           return leftIs and rightIs


### 补充知识点


