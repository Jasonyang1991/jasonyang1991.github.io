---
title: "Python copy and deep copy"
date: 2020-02-28T19:57:35+01:00
tags: ["Python"]
categories: ["Skills"]
draft: false
comments:       true
showMeta:       true
showActions:    true
thumbnailImagePosition: "left"
thumbnailImage: /img/copy.png
---

Python 的复制有浅复制和深复制之分:

<!--more-->

## 等于号

```python
import copy
a = [1,2,3]
b = a
id(a) #  id() 函数用于获取对象的内存地址
>>> 139935155645768
id(b)
>>> 139935155645768
print(id(a)==id(b)) #  可以发现 a b 的对象内存地址完全相同
>>> True
b[0] = 11 # 此时改变b
print(a)
>>> [11,2,3] # a 随之改变
a[1] = 22
print(b)
[11,22,33] # 同理
```

使用等于号，则两者的对象内存地址完全相同，两者改变互相牵连。

## 浅复制

```python
import copy

# shallow copy
a = [1,2,[3,4]]
b = a
d = copy.copy(a) # copy.copy 潜复制
print(id(a)==id(d))
>>> False #  发现 a d 列表的第一层的对象内存地址不同
print(id(a[2]) == id(d[2])) # 但是第二层对象内存地址相同
d[1] = 222222
print (a)
>>> [11,22,3]
ptint (d)
>>> [11,222222,3]
d = [1,2,[3,4]]
```

浅复制中列表的第一层指向不同的储存位置，两者不会互相改变。但是第二层指向相同的储存位置，改变是互相牵连的

## 深复制

```python
# deep copy
a = [1,2,[3,4]]
c = copy.deepcopy(a)
print(id(a) == id(c))
c[1] = 2
print(a)
a[1] = 111
print(c)
>>>
False
[1, 2, [3, 4]]
[1, 2, [3, 4]]
```

深复制是完完全全的复制，所有的元素的指向不同的对象内存地址。