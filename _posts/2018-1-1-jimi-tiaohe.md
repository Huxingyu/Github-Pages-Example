---
layout: post
title: 对于调和级数与P-级数收敛性的证明
description: 这两个老哥有点意思
category: blog
---
<html>

<head>
<title>MA_0001_发散与收敛</title>
</head>

<body>
在这里我们研究形式如\(\frac {1}{n^p}\)级数发散与收敛的性质
<p>
我们首先对\(\frac {1}{n^p}\)进行观察，分类：
</p>
$$
S(n) =
\begin{cases}
\sum_{n=1}^\infty \frac {1}{n^p},&\text{p\(\le\)1} \\
\sum_{n=1}^\infty \frac {1}{n^p},&\text{p\(\gt\)1}
\end{cases}
$$
<p>(1)对于\(p\le\)1的情况，我们只需要证明\(p=1\)的情况即可，这个条件的成立在于\(p=1\)是发散的，因为\(p=0\)或者负数的情况是平凡的，可以简单推出。</p>
<p>我们可以通过反证法对其进行证明：</p>
<p>假设\(p\le\)1的情况下级数是收敛的，并且绝对收敛于\(s\)，记为：</p>

$$
\lim\limits_{n \to \infty}S(n)=s
$$
<p>则有：</p>
$$
\lim\limits_{n \to \infty}S(2n)=s
$$
<p>即有：</p>
$$
\lim\limits_{n \to \infty}[S(2n)-S(n)]=0
$$
<p>而我们利用级数展开进行计算可知：</p>
$$
\begin{equation}\begin{split} 
S(2n)-S(n)&=[\frac {1}{1}+\frac {1}{2}+\ldots+\frac {1}{n}+\frac {1}{n+1}+\ldots+\frac {1}{n+n}]-[\frac {1}{1}+\frac {1}{2}\ldots+\frac {1}{n}]\\
&=\frac {1}{n+1}+\frac {1}{n+2}+\ldots+\frac {1}{n+n}\\
&\gt\frac {1}{n+n}+\frac {1}{n+n}+\ldots+\frac {1}{n+n}\\
&=\frac {n}{n+n}\\
&=\frac {1}{2}
\end{split}\end{equation}
$$
<p>由此可知与之前猜想相互矛盾，所以\(S(n)\)收敛猜想不成立。</p>
<p>对于证明\(p>1\)时的情况，我们不能使用初等方法给出，由于时间关系，我会另外写出证明\(P-\)级数收敛的方法，而且其与黎曼\(\xi\)函数相等，一个比较深刻的结论。</p>
<p>2018快乐，祝自己新的一年一切顺利。</p>
</body>

</html>
<script type="text/javascript"
   src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>


