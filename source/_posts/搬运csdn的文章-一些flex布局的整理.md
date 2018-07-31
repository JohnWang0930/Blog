---
title: 搬运csdn的文章[一些flex布局的整理]
date: 2018-07-31 15:55:17
tags:
---

>hi all,好久没上csdn发文章了，不知不觉离上一次发文章已经过去了四个月时间，这段时间一直在公司学习并且实践，为了记录自己的学习， 立个fleg，从今天开始要勤发文章！

---
>很久之前在学flex，今天就稍微整理一下发上来，希望大家能够提出意见和建议哈。

---
### Flex
#### flex容器属性：
- flex-direction：
 - rows(水平)
 - row-reverse（反向水平）
 - column（垂直）
 - column-reverse（反向垂直）
- flex-wrap：
 - nowrap（不换行）
 - wrap（换行）
 - wrap-reverse（换行，第一行在下面）
- flex-flow：（上述两行的简写，以" "分割）
 - justify-content：
 - flex-start（主轴起始位置对齐）
 - flex-end（主轴结束位置对齐）
 - center（中间对齐） 
 - space-between（与两端对齐，间距相等）
 - space-around（两侧的间隔相等，两个子元素间距离double）
- align-items：
 - stretch（如果子元素未设置高度或设为auto，占满）
 - flex-start
 - flex-end
 - center
 - baseline（第一行文字的基线对齐）
- align-content：（多行、多列情况，交叉轴对齐方式）
 - flex-start
 - flex-end
 - center
 - space-between
 - space-around
 - stretch
 
#### flex容器下子元素属性：
- order：（排列顺序，value为数字，默认为0）
 - flex-grow：（子元素放大比例，默认为0，不缩放）
 - flex-shrink：（子元素缩小比例，默认为1，等比缩小，设置成0时不缩小）
 - flex-basis：（子元素缩放前，占主轴空间，默认auto）
- flex：（上述三项简写 默认0 1 auto，可填auto（代表1 1 auto）、none（代表0 0 auto）或分开写）
- align-self：(自我的align-item属性，auto继承父元素)
 - auto
 - flex-start
 - flex-end
 - center
 - baseline
 - stretch