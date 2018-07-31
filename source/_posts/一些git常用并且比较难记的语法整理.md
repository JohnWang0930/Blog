---
title: 一些git常用并且比较难记的语法整理
date: 2018-07-31 23:12:38
tags:
---

> 今天上午用git整这个博客，感觉还是有些语句用的不顺手  
> 下午就顺便缕了一遍git常用的一些语法，这里记录一些**常用且难记的语法**

1. 撤回工作区的文件修改/撤回暂存区的文件修改

```
git checkout -- filename
```

2. 撤销add到暂存区的操作

```
git reset head filename
```

3. 首次创建ssh Key

```
ssh-keygen -t rsa -C "email"
```

4. 本地库与远程库关联

```
git remote add origin XXX
```

5. 删除分支

```
git branch -d name
```

6. 查看日志

```
git reflog
git log
git log --graph(分支合并图)
```

7. 添加本地未提交的文件到stash

```
git stash
git stash list
git stash pop
```

8. 删除远程分支

```
git push origin :远程分支
```

