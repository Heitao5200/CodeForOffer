## 平台
牛客网

## 语言
python2.7.3

## 作业内容

### 题目描述
* 输入一个整数数组，
* 实现一个函数来**调整该数组中数字的顺序，**
* 使得所有的奇数位于数组的前半部分，所有的偶数位于数组的后半部分，
* 并保证奇数和奇数，偶数和偶数之间的相对位置不变。



### 题目理解
数组的排序问题



### 解题思路
    对于给定的数组，
    定义两个空列表
    遍历
      当遍历到的数是奇数时，添加到第一个空列表
      当遍历到的数是偶数时，添加到第二个空列表
    两个列表拼接




### 程序

    class Solution:
        def reOrderArray(self, array):
            odd = []
            even = []
            for i in array:
                if i%2==1:
                    odd.append(i)
                else:
                    even.append(i)
            return odd + even


### 补充知识点
[python中对列表的所有操作方法](https://blog.csdn.net/kingsm06507/article/details/76735906)

* list和array的相互转换

    u = array([[1,2],[3,4]])
    m = u.tolist()   #转换为list
    m.remove(m[0])    #移除m[0]
    m = np.array(m)    #转换为array