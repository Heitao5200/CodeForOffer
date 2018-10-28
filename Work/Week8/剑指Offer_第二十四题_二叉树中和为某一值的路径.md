## 平台
牛客网

## 语言
python2.7.3

## 作业内容

### 题目描述
输入一颗二叉树的跟节点和一个整数，打印出二叉树中结点值的和为输入整数的所有路径。

路径定义为从树的根结点开始往下一直到叶结点所经过的结点形成一条路径。

(注意: 在返回值的list中，数组长度大的数组靠前)




### 题目理解

找路径(根节点往子节点连)

路径中的元素之和为注入的整数


### 解题思路



1. 如果只有根节点或者找到叶子节点，我们就把其对应的val值返回

2. 如果不是叶子节点，我们分别对根节点的左子树、右子树进行递归，直到找到叶子结点。然后遍历把叶子结点和父节点对应的val组成的序列返回上一层；如果没找到路径，其实也返回了序列，只不过是[]



### 程序
    class Solution:
        # 返回二维列表，内部每个列表表示找到的路径
        def FindPath(self, root, expectNumber):
            # write code here
            if not root:
                return []
            if root and not root.left and not root.right and root.val == expectNumber:
                return [[root.val]]
            res = []
            left = self.FindPath(root.left, expectNumber-root.val)
            right = self.FindPath(root.right, expectNumber-root.val)
            for i in left+right:
                res.append([root.val]+i)
            return res



### 补充知识点
