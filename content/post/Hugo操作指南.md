---
title: "Hugo操作指南"
date: 2018-06-27T12:57:59+02:00
tags: ["Hugo"]
categories: ["Skills"]
draft: false
comments:       true
showMeta:       true
showActions:    true
thumbnailImage: /img/IMG_7666.JPG
coverImage: /img/IMG_7666.JPG
metaAlignment: center
---
这篇Bolg将记录Hugo使用过程中的一些心得和技巧

<!--more-->

<!-- toc -->

# Hugo Tutorial
可以参考YouTube上[Giraffe Academy](https://www.youtube.com/channel/UCvmINlrza7JHB1zkIOuXEbw/playlists)的视频

# 插入目录

`<!-- toc -->`

# 图片

* 插入本地图片需将图片存放在`static`目录下：

      `![图片备注](/pic.png)`

      需注意： `.JPG` `.jpg` 等大小写问题将导致引用失败

* 插入网络图片：

      `![图片备注](/https://avatars2.githubusercontent.com/u/3265208?v=3&s=100 "GitHub,Social Coding)`
