## 平台
牛客网

## 语言
python2.7.3

## 作业内容

### 题目描述
    请实现一个函数，将一个字符串中的每个空格替换成 “%20”。
    例如，当字符串为 We Are Happy. 则经过替换之后的字符串为 We%20Are%20Happy    
    
### 题目理解
    字符串的操作有哪些
    



### 解题思路
字符串的替换方法


### 程序
    # -*- coding:utf-8 -*-
    import re
    class Solution:
        # s 源字符串
        def replaceSpace(self, s):
            # write code here
            return re.sub(" ","%20",s)


### 补充知识点
#### python 中字符串的常见操作
如果我们想要查看以下功能：help（mystr .find）

* find

    例：mystr=“hello world itcast”  mystr.find("hello")  结果为 6

    find 括号中填写要查找的内容，如果找不到返回 - 1，找到返回从左往右找到的第一个位置

* index

    功能和 find 一样，只是找不到时，这个返回错误

* rfind

    从右往左找的第一个位置

* rindex

    从右往左找

* count

    统计字符串中出现的次数，没有出现一次返回 0

    例：mystr.count("itcast") 结果为 1

* replace

    替换，参数 1：源  参数 2：目标  但是原来的并没有改变，只是显示一次改变的结果，因为这是不可变类型，除非用一个变量重新接收

    例：mystr.replace("world","WORLD") 用大写的替换小写的值

* split

    切割

    例：mystr.split("") 把有空格的都切割掉，按照空格切，按什么来切，什么就会没有，保存格式为列表的格式

* capitalize

    把第一个字母变成大写

    mystr.capitalize()

    'Hello world itcast'

* title

    字符串的每个首字母都大写

    mystr.title()

    'Hello World Itcast'

* startswitch

    检查字符串是否以某个字符串开头，是返回 true，否返回 false  mystr.startswitch(obj)

* endwith

    检查字符串是否以某个字符串结尾

* lower

    转换 mystr 中所有大写字符为小写

* upper

    转换 mystr 中所有小写字符为大写

* ljust  rjust

    返回一个原字符串左（右）对齐，并使用空格填充至长度 width 的新字符串

    mystr.ljust(10) 长度不够的用空格填充

* center

    返回一个原字符串居中，并使用空格填充长度 width 的新字符串

* lstrip rstrip strip

    删除 mystr 字符串前端的空白字符
    
    删除 mystr 字符串末端的空白字符
    
    删除 mystr 字符串两端的空白字符
       
    如果要删除多个不同字符串前后的空白字符和有 \ t 出现的情况 mystr.split() 就什么都不加

* partition

    把 mystr 以 str 分割成三部分，str 前，str 和 str 后
    
    mystr=‘hello world itcast and it’
    
    mystr.partition("itcast")
    
    （‘hello world’，‘itcast’，‘and it’）

* rpartition lpartition

    从右边和从左边开始

* splitlines
    
    按照行分隔，返回一个包含各行作为元素的列表，按换行来切割
    
    mystr="hello\nworld"
    
    mystr.splitlines()
    
    结果为：['hello','world']

* isalpha

    如果 mystr 所有的字符都是字母，返回 true
    
    mystr.isalpha()

* isdigit

    判断是不是等于纯数字的字符串

* isalnum

    是不是字母和数字组合在字符串中

* isspace

    判断是不是纯空格

* join

    把字符串连接在一起

    例：names=["aaa","bb","cc"]

    a="_"

    a.join(names)

    结果为：aaa_bb_cc

