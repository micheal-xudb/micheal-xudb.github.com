---
layout: post
title: "python list comparations"
description: ""
category: 
tags: []
---
{% include JB/setup %}

列表解析和生成表达式

需要改变列表而不是新建列表时，用列表解析（list comprehensions）

[expr for iter_var in iterable]
[expr for iter_var in iterable if cond_expr]

例子：
>>> L= [(x+1,y+1) for x in range(3) for y in range(5)]
>>> L
[(1, 1), (1, 2), (1, 3), (1, 4), (1, 5), (2, 1), (2, 2), (2, 3), (2, 4), (2, 5), (3, 1), (3, 2), (3, 3), (3, 4), (3, 5)]
>>> N=[x+10for x in range(10) if x>5]
>>> N
[16, 17, 18, 19]

生成表达式得到一个可迭代的 generator object

(expr for iter_var in iterable)
(expr for iter_var in iterable if cond_expr)

>>> L= (i +1for i in range(10) if i %2)
>>> L
<generator object <genexpr> at 0xb749a52c>
>>> D=[]
>>>for i in L:
... D.append(i)
...
>>> D
[2, 4, 6, 8, 10]