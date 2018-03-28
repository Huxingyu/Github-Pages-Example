---
layout: post
title: 欧几里得算法实现与最大公约数算法研究
description: 小而美。
category: blog
---

欧几里德算法形式很简单，形式与证明都十分的容易，但是却广泛的应用在各个科学领域的边角，这里对其进行证明与语言实现版本给出。

核心算法：$$gcd(a,b)=gcd(b,a\mod b)$$

数学证明：
--

- 正向

设$$a=kb+r$$,则有$$r=a mod b$$;

再设$$d$$为$$a$$,$$b$$公约数,则有:$$d\|a$$,$$d\|b$$。

由于$$a=kb+r$$,则有$$r=a-kb$$。

故$$d$$为$$(b,a mod b)的公约数。

- 逆向

设$$d$$为$$(b,a\mod b)$$的一任意公约数，

则有$$d\|b,$$d\|r$$，而$$a=kb+r$$.

故$$d$$为$$(a,b)$$公约数。

高级语言实现
--

- C++语言平凡情形

~~~
int gcd(int a,int b){
    if(b==0){
        return a;
    }
    return gcd(b,a%b);
}
~~~

- C++语言迭代情形

~~~
int gcd(int a,int b){
    int t;
    while(t){
        t=a%b;
        a=b;
        b=t;
    }
    return a;
}
~~~

扩展欧几里得算法
--

Stein算法
--

连分数联系
--

几何拓扑联系
--

