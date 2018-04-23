---
layout: post
title: Something in Fourier Analysis
description: 万丈高楼平地起，莫在浮沙筑高台，整理一下基于数学和物理角度上的Fourier Analysis；工程上的简化虽好，可不要贪杯奥。
category: blog
---

> ###"美丽有两种. 一是深刻又动人的方程. 一是你泛着倦意淡淡的笑容。"

> ###最近喜欢上了一个女孩，借先辈UKIM的这句很抒情的话抒情下吧。


Wave equation
--

——————0——0——0——0————...————————

考虑如上十分简陋的一列质量为$$m$$的小质点（即0），相邻之间的长度为$$h$$，弹簧（即折线）的弹簧劲度系数为$$k$$，则我们有：

$$F_{Newton}=m\cdot a(t)=m\cdot \frac {\partial^2}{\partial t^2}\cdot u(x+h,t)$$
$$F_{Hooke}=F_{x+2h}+F_{x}=k[u(x+2h,t)-u(x+h,t)]+k[u(x,t)-u(x+h,t)]$$

由分析力学中的达朗贝尔原理，位于$$x+h$$处质点的运动方程为：

$$m\cdot \frac {\partial^2}{\partial t^2}\cdot u(x+h,t)=k[u(x+2h,t)-2u(x+h,t)+u(x,t)]$$

如果我们规定，有$$N$$个质点作用在$$L=Nh$$长度的弹簧上，总质量为$$M=Nm$$,其中链的总劲度系数为$$K=k/N$$,则总体的运动方程为:

$$\frac {\partial^2}{\partial t^2}\cdot u(x+h,t)=\frac {KL^2}{M}\cdot \frac {u(x+2h,t)-2u(x+h,t)+u(x,t)}{h^2}$$

我们取$$N\rightarrow\infty$$,$$h\rightarrow 0$$，则有

$$\frac {\partial^2}{\partial t^2}\cdot u(x+h,t)=\frac {KL^2}{M}\cdot \frac {\partial^2 u(x,t)}{\partial x^2}$$

这就是著名的偏微分方程————弦振动方程。













