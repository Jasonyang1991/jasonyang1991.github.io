---
title: "Python 文件读写"
date: 2020-02-27T15:02:24+01:00
tags: ["Python"]
categories: ["Skills"]
draft: False
comments:       true
showMeta:       true
showActions:    true
thumbnailImagePosition: "left"
thumbnailImage: /img/Write.png
---

Python 内置了文件IO的函数：

<!--more-->

- 写入文件
  - 首先打开（创建）一个文件，可以以 txt 形式纯村
  - 然后写入数据
  - 最后关闭文件

```python
my_file = open('my_file.txt','w') 
# w for write, r for read, a for append(追加内容)

text = 'This is 1st line.\nThis is 2nd line.\nThis is 3rd line.'
# \n 换行 

my_file.write(text)
my_file.close()
```

- 读取文件
  - 打开文件
  - 读取内容

```python
file = open('my_file.txt','r')
content = file.read()
print(content)

>>>
This is 1st line.
This is 2rd line.
This is 3rd line.
```

使用 readline 命令可以逐行读取。