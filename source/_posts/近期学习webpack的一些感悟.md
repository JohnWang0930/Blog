---
title: 近期学习webpack的一些感悟
date: 2018-08-06 23:22:59
tags:
---
> 最近在学习webpack，从刚开始的云里雾里到现在略懂一二

刚开始学webpack，手头上正好有小程序项目，所以方向是结合小程序写一个webpack

目前小程序的技术栈：原生小程序+scss

尝试了几天发现小程序并不适用于webpack打包，几个原因:

1. 微信开发工具会进行打包压缩上传，所以必须使用不同chunk作为页面
2. webpack会将引入资源打包到当前chunk内，产生重复代码（没有实现commonchunk，原因是不知道怎么实现自动改变引入资源路径）

> 此处因为这些原因，所以转换思路为：保持目录结构不变，实现1.babel降级实现async等微信不支持的es6语法 2.scss编译

后期方向：使用node制作一个脚本实现如上两个功能（最好能够实现watch功能）