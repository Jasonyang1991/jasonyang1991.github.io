---
title: "Python多变量赋值操作"
date: 2020-02-27T13:41:05+01:00
tags: ["Python"]
categories: ["Skills"]
draft: false
comments: true
showMeta: true
showActions: true
thumbnailImagePosition: "left"
thumbnailImage: /img/python-icon.png
---

Python 对多变量同时赋值实际上是一种自动解包 Unpacking 的操作。

<!--more-->

```python
a,b,c = 1,2,3
print(a,b,c)
>>> 1 2 3
```

类似的解包还有：

元组解包：

```python
a,b,c = (1,2,3)
print (a)
print (b)
print (c)
>>>1
>>>2
>>>3
```

字符串解包：

```python
a,b,c = 'abc'
print (a)
print (b)
print (c)
>>>a
>>>b
>>>c
```

字典解包：

```python
a,b,c = {'d':1, 'e':2, 'f':3}
print (a)
print (b)
print (c)
>>>d
>>>e
>>>f
```

字典解包则会丢失value。