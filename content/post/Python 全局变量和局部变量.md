---
title: "Python 全局变量和局部变量"
date: 2020-02-27T14:34:50+01:00
tags: ["Python"]
categories: ["Skills"]
draft: false
comments:       true
showMeta:       true
showActions:    true
thumbnailImagePosition: "left"
thumbnailImage: /img/variable.png
---

局部变量是在函数内部使用的变量，和函数外部没有关系：

<!--more-->

```python
x = 50      #全局变量
def func1():
    x = 20      #局部变量
    print ('local x: ', x)

func1()
print ('global x: ', x)

# 结果如下， 函数内的赋值并没有影响到函数外 x 的值
>>>local x:  20
>>>global x:  50
```

想让函数内部的变量变成全局变量则需使用 global：

```python
x = 50      #全局变量
def func1():
    global x    #定义全局变量
    x = 20      #定义后的 x 变量可以在全局范围内更改
    print ('local x: ', x)

func1()
print ('global x: ', x)

# 函数内的赋值更改了函数外 x 的值
>>>local x:  20
>>>global x:  20
```

