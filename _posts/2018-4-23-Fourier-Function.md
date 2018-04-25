---
layout: post
title: Something in Fourier Analysis
description: 万丈高楼平地起，莫在浮沙筑高台。
category: blog
---

"美丽有两种. 一是深刻又动人的方程. 一是你泛着倦意淡淡的笑容。"

最近喜欢上了一个女孩，借UKIM的这句很抒情的话抒情下吧。
我希望对后一种美丽，最后有可解的答案。


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

令$$c=\sqrt {\frac {KL^2}{M}}$$
则波动方程可表示为算子形式：$$[\frac {\partial}{\partial t}-c\frac {\partial}{\partial x}][\frac {\partial}{\partial t}+c\frac {\partial}{\partial x}]u=0$$
则其通解可表示为：$$u(x,t)=F(x+ct)+G(x-ct)$$考虑初值条件:
$$\begin{cases}u(x,0)=f(x)\\u_{t}(x,0)=g(x)\end{cases}$$
代入可得达朗贝尔行波解：$$u(x,t)=\frac {f(x-ct)+f(x+ct)}{2}+\frac {1}{2c}\int_{x+ct}^{x-ct}g(s)ds$$
分离变数法与Sturm-Liouville问题--
$$ \left\{\begin{array}{rcl}(D.E.)     & {\frac {\partial^2 u}{\partial t^2}=c^2\frac {\partial^2 u}{\partial x^2 ,}} &{0\leq x \leq L ,} &{0 \leq t}\\(B.C.)         & {u(0,t)=u(L,t)=0 , }& {0\leq t}\\(I.C.)     & {u(x,0)=f(x) ,} & {\frac {\partial u}{\partial t}(x,0)=g(x) ,} & {0 \leq x \leq L}\\\end{array} \right. $$
根据伯努利分离变数法，可设$$u(x,t)=T(t)\varphi(x)$$
$$ \left\{\begin{array}{rcl}T''(t)+c^2\varphi ^2T(t)=0\\\varphi''(x)+\varphi(x)=0 ,& {\varphi(0)=\varphi(L)=0}\end{array} \right. $$
根据固有值问题我们可令：
$$\lambda_{n}=(\frac {n\pi}{L})^2$$,$$(x)=sin\frac {n\pi x}{L}$$
将\lambda_{n}代入T满足的方程，令T解为：$$T_{n}(x)=a_{n}cos\frac{n\pi ct}{L}+b_{n}sin\frac{n\pi ct}{L}$$
根据初值与正交可确定傅里叶系数，最终我们得到傅里叶级数为:
$$f(x)=\sum_{-\infty}^{+\infty}C_{n}e^{i\frac{n\pi x}{2}}$$
其中$$c_{n}$$为$$c_{n}=\frac {1}{2L}\int_{-L}^{l} f(x)\cdot e^{i\frac {n\pi x}{2}}dx$$

之后傅里叶将函数由$$(-L,+L)$$推广至无穷，得到我们现在常用的傅里叶变换，下面给出现代分析中的定义:
$$\hat{f}(\xi)=\int_{\mathbb{R}}e^{-2\pi ix\cdot\xi}f(x)dx,\xi\in\mathbb{R}$$
后面还会有好多工作，不过不在今天和这篇文章里面写了，有些累喽。今天写的内容，里面还有一些不清晰的，需要查阅一些资料。










