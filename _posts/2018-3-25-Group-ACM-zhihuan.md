---
layout: post
title: 交换群在几何与组合中的应用
description: 分两条路径，体会一下群论的POWER，一从几何，一从组合（ACM）。蜻蜓点水，希望对以后的工作能有所帮助。
category: blog
---

这周接连两个重量级的科学奖公布了名单，一是数学的阿尔贝奖，一是计算机的图灵奖。

阿尔贝奖给了朗兰兹，可以说是实至名归了。恰恰这周主要在学习群论之中的知识，朗兰兹最著名的莫过于其提出的朗兰兹纲领，19世界也有一个特有名的纲领，即是克莱因的爱尔兰纲领，是联系群论与几何的一条路。这条路的基石就是变换群与几何不变量之间的关系。

与变换群一个十分相仿的概念是置换群，其常常作用于组合数学的计数之中，在ACM题目中常见，比如2001年国家集训队队员符文杰的论文《Pólya原理及其应用》。个人现在学的不好，老是感觉这两个群差不多，也说不出这两个群可不可以进行交叉的应用，随着学习的深入之后再来回答吧。

先给出它们两个基础的定义：

![jiaohuan](/images/math/group/001.JPG)

- 定义1：非空集合$$A$$的所有一一变换关于变换的乘法所作成的群叫做$$A$$的一一变换群，用$$E(A)$$表示，$$E(A)$$的子群叫做变换群。

- 定义2：当$$A$$是一个有限集合时，$$A$$中的一个一一变换称为一个$$n$$元置换，由置换构成的群叫做置换群。因此置换群是变换群的一个特殊类型。
