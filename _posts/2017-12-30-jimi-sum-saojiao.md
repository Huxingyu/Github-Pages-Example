---
layout: post
title: 吉米多维奇中一道三角函数求和题目
description: 利用了欧拉公式与棣莫弗定理，可以从中研究一下这两个定理之间的关联
category: blog
---

来自吉米多维奇数学分析习题集第\(2551\)题目，有一些有意思的地方：


$$\sum_{n=1}^\infty f(n) = qsin\alpha + q^2sin\alpha^2 + \cdots + q^nsin\alpha^n + \cdots （\lvert q \rvert <1）$$



1，求解$$f(n)$$连加之和. 

2，若上式中$$sin\alpha$$换为$$cos\alpha$$，则其$$\sum_{n=1}^\infty f(\alpha)$$会发生什么变化，结果是多少.

解决思路：这个题目的有趣之处在于1,2问是在一块的，思路对了可以两个同时解出，否则1，2全都解决不了。

关键思想在于,若我们假设：
$$
z=q(cos\alpha + isin\alpha)
$$


则有：


$$
f(n) =
\begin{cases}
\sum_{n=1}^\infty z^n=\sum_{n=1}^\infty q^ncosn\alpha + i\sum_{n=1}^\infty q^nsinn\alpha,&\text{(1)} \\
\sum_{n=1}^\infty z^n=\frac {1}{1-z}=\frac {1}{1-qcos\alpha-iqsin\alpha},&\text{(2)}
\end{cases}
$$


我们只需要比较$$(1)(2)$$对应的虚实部分即可得出:



对于$$(2)$$我们有化简


$$
\frac {1}{1-qcos\alpha-iqsin\alpha} = \frac {(1-qcos\alpha)+iqsin\alpha}{1-2qcos\alpha+q^2},     (3)
$$
<dr/>


之后比较$$(1)(3)$$，我们容易得到1，2问的全部结果。


这个问题答案使用了一个原来没有见过的公式，即棣莫弗定理：

\begin{equation}\begin{split} 
cos(nx) + isin(nx)&= (cosx + isinx)^n\\
&=\sum_{k=0}^n[C_n^k(isinx)^n(cosx)^{n-k}]
\end{split}\end{equation}

* 下面完成对这个公式的证明
* 并且给出其与欧拉公式的内在联系

<script type="text/javascript"
   src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>


<script type="text/javascript"
   src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>
