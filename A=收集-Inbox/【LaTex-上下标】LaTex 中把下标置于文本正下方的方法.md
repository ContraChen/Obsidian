---
alias: Latex上下标
tags: area/ot/latex
---

> 本文由 [简悦 SimpRead](http://ksria.com/simpread/) 转码， 原文地址 [blog.csdn.net](https://blog.csdn.net/da_kao_la/article/details/84836098)

在使用 [LaTex](https://so.csdn.net/so/search?q=LaTex&spm=1001.2101.3001.7020) 进行排版时，一个常见的需求是要把下标放在某个文字或者符号的正下方：

![](https://private.codecogs.com/gif.latex?f_3%28d%29%20%3D%20%5Cmathop%7Bmax%7D%5Climits_%7Bx_3%7D%282x_3%20&plus;%20f_4%28d-x_3%29%29)

LaTex 的数学模式下提供了 **\limits** 命令，形如

```
expr1\limits_{expr2}^{expr3}

```

中 expr2 会出现在 expr1 的正下方，而 expr3 会出现在 expr1 的正上方，例如命令

```
$\sum\limits_{i=0}^n {x_i}$

```

会生成效果

![](https://private.codecogs.com/gif.latex?%5Csum%5Climits_%7Bi%3D0%7D%5En%7Bx_i%7D)

但是 \ limits 命令要求 expr1 必须的数学符号，否则会报错：

```
! Limit controls must follow a math operator.

```

但是有时我们需要上 / 下标出现在一段非数学符号的正上 / 下方，如本文开头的需求，这时应该怎么办呢？

解决方法是用 **\mathop**{expr1} 命令将 expr1 转化成数学符号，写成

```
\mathop{expr1}\limits_{expr2}^{expr3}

```

这样就可以使用 \ limits 命令了，例如命令

```
$f_3(d) = \mathop{max}\limits_{x_3}(2x_3 + f_4(d-x_3))$

```

会生成效果

![](https://private.codecogs.com/gif.latex?f_3%28d%29%20%3D%20%5Cmathop%7Bmax%7D%5Climits_%7Bx_3%7D%282x_3%20&plus;%20f_4%28d-x_3%29%29)