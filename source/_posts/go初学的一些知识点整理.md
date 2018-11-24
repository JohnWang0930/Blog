---
title: go初学的一些知识点整理
date: 2018-11-24 23:11:35
tags:
---

> Hi all 好久没更新博客了，最近在学go，期间写了一个简单的发邮件脚本，地址可以参照[goDeno](https://github.com/JohnWang0930/sendEmail) 如果有任何意见和建议 可以给我留言哈。  

> 下面简单列一些知识点，不会按照体系列出来，纯粹是个人认为的一些比较重要的知识点。  

- `func main`一定要在`main`包内

- 在同一个文件夹中的包必须是同样的包名

- `import _ '...'` 执行`...`包内`init`函数

- 所有`init`函数都在`main`包前执行

- 变量声明时建议
    > 需要用零值时用var声明
    > 不需要用零值时用make()声明

- `a,b:=map["key"]`此时`a`表示值 `b`表示是否存在`key`键所对应的值 不存在时`a`为该类型零值

- `defer`定义的后执行函数，在程序崩溃是也会运行

- 初始化
    > `new`返回指针并初始化为零值（大多可用短声明/结构体字面亮取代）
    > `make`只作用域非典型类型`slice、map、chan、interface、func`返回非零值

- `range chan类型`时会一直循环且阻塞知道`chan`被close

- 包查找顺序`./vendor -> GOROOT -> GOPATH`


先写到这 晚点有空再更新这篇博客