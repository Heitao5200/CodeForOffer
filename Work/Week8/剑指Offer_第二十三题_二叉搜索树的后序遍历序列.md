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
        def VerifySquenceOfBST(self,sequence):
            # write code here
            if len(sequence)==0:
                return False
            index = 0
            for i in range(len(sequence)):
                if sequence[i]>sequence[-1]:
                    index = i
                    break
            for j in range(i,len(sequence)):
                if sequence[j]<sequence[-1]:
                    return False
            left = True
            right = True
            if len(sequence[:index])>0:
                left = self.VerifySquenceOfBST(sequence[:index])
            if len(sequence[index:-1])>0:
                right = self.VerifySquenceOfBST(sequence[index:-1])
            return left and right


### 补充知识点


