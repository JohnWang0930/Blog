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

- 初始化函数执行顺序：导入顺序a->b->c；init函数执行顺序c->b->a->main

- 数组特性
1. 长度固定
2. 下标紧邻
3. 类型相同
4. 内存连续分配
5. 索引快

- 切片包含
1. 指向底层连续内存的指针
2. 长度
3. 最大容量

- 切片超出容量时，会创建新的底层数组并复制原来储存的内容，容量<=1000时增加100%，反之则增加25%

- len（x）返回长度 cap（x）返回容量

- 引用类型:slice map func chan interface 除此之外的类型都是值类型

- `runtime.GOMAXPROCS(runtime.NUMCPU())`能够为每个核创建一个线程

- 两个goroutine同时对一个变量进行值操作可能会引起竞争，解决办法：用`atomic.AddInt64`、`mutex.Lock()`、`chan`等方法进行解决

