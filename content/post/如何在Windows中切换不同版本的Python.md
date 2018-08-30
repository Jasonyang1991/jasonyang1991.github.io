---
title: "Windows 中 Python 版本的控制"
date: 2018-08-30T22:29:25+02:00
categories:
- Skills
tags:
- Anaconda
- Python

comments:       true
showMeta:       true
showActions:    true
thumbnailImagePosition: "right" #封面位置 top， right, left or bottom
thumbnailImage: https://realpython.com/static/pytrick-dict-merge.4201a0125a5e.png
metaAlignment: center
---

由于 caffe 只支持到 Python3.5，但是 Anaconda 的最新版本是 Python3.6，产生了 Python 不同版本切换的需求。

`<!--more-->`

Windows 下不同 Python 版本的控制主要通过 Anaconda 来完成，所有的命令都可以在以管理员身份运行的`cmd`中完成。

* 安装[最新版本的 Anaconda](https://www.anaconda.com/download/)

* 查看目前Python版本，直接在`cmd中输入

```
python
```
得到目前的版本为 Python3.6

```
Python 3.6.5 |Anaconda, Inc.| (default, Mar 29 2018, 13:32:41) [MSC v.1900 64 bit (AMD64)] on win32
```

* 使用命令创建新的环境

  ```
  conda create -n py35 python=3.5 anaconda
  ```

  这将创建一个基于`python3.5`，名为`py35`的新环境

  ```
  conda create -n py27 python=2.7 anaconda
  ```

  想安装`python2.7`可以使用这条命令

* 列出所有的环境

  ```
  conda info --envs
  ```

  检查到 anaconda information for environments

  ```
  # conda environments:

base                  *  C:\Users\yangj\Anaconda3
py35                     C:\Users\yangj\Anaconda3\envs\py35

  ```

  可以通过`*`判断出，目前活动的环境是名为`base`的`环境`

* 切换到另一环境，只需输入 activate 命令以及另一个环境的名字

  ```
  activate py35
  ```

参考资料：

* [Anaconda多环境多版本python配置指导](Anaconda多环境多版本python配置指导)
* [Determining your current environment](https://conda.io/docs/user-guide/tasks/manage-environments.html#determining-your-current-environment)
* [Installing a different version of Python](https://conda.io/docs/user-guide/tasks/manage-python.html#installing-a-different-version-of-python)
