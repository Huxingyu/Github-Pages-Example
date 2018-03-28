---
layout: post
title: 随机过程中一些基础定理的数学推导
description: 随机过程作为通元的先修，一些概念不好理解，现在给出具体的推导，step by step.
category: blog
---

通信系统中的信号与噪声都具有一定的随机性，所以我们需要用随机过程这一工具进行分析。

![sum](/images/communicaton/random_process/SUM.JPG)

这是大致的章节，分为6部分，下面一一给出。

一，基本概念
--

![sum](/images/communicaton/random_process/001.JPG)

1,随机过程的分布函数

**累计分布函数**，又叫**分布函数**，是概率密度函数的积分，能完整描述一个实随机变量X的概率分布。定义：

$$F_X(x)=P(X<x)$$

X之值落在区间(a,b]之内的几率为：

$$P(a<X<b)=F_X(b)-F_X(a)$$

一随机变数$X$的CDF与其PDF的关系为：

$$F_X(x)=\int_{-\infty}^x f_X(t)dt$$
