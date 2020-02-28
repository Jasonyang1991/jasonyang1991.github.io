---
title: "Python 错误处理"
date: 2020-02-28T19:07:44+01:00
tags: ["Python"]
categories: ["Skills"]
draft: false
comments: true
showMeta: true
showActions: true
thumbnailImagePosition: "left"
thumbnailImage: /img/error.png
---

Python 内嵌了错误处理的机制: <!--more-->用 try 可以确定某一段代码是否有错误，以及错误的原因。

```python
try:
    print('start trying r = 10 / z ')
    z = 0
    r = 10 / z
    print('result:', r)
except ZeroDivisionError as e:
    print('except:', e)
    response = input ('do you want to change the value of z')
    if response == 'y':
      print('go change it')
else:
  print('no error')
finally:
    print('Thats it')
print('END')
>>>
start trying r = 10 / z 
except: division by zero
do you want to change the value of z
y
go change it
Thats it
END
```

- 首先尝试计算
- 然后储存错误信息，并作出提示
- 对错误信息进行处理
- 如果有错误就执行 except 里的语句，没有错误就执行 else 语句
- 执行 finally 语句

```python
try:
    print('start trying r = 10 / z ')
    z = 2 # 现在对 z 值修改，重新计算
    r = 10 / z
    print('result:', r)
except ZeroDivisionError as e:
    print('except:', e)
    response = input ('do you want to change the value of z')
    if response == 'y':
      print('go change it')
else:
  print('no error')
finally:
    print('Thats it')
print('END')
>>>
start trying r = 10 / z 
result: 5.0
no error
Thats it
END
```