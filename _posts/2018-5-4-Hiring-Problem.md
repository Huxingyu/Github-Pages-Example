---
layout: post
title: The mathematical principle and code of Hiring Problem
description: 此情可待成追忆，只是当时已惘然--说的就是这个问题。
category: blog
---

Problem's Describe
--
Hiring Problem,it is also known as the Secretary Problem,we use the wikipedia definiton to define it.

**The basic form of the problem is the follwinng:imagine an administrator who wants to hire the best secretary out of $$n$$
rankable applicants for a position.The applicants are interviewd one by one in random order.A decision about each particular appliant is to be made immediately after the interview.Once rejectd,an applicant cannot be recalled.During the interview,the administrator can rank the applicant among all interviewd so farm,but is unaware of the quailty of yet unseen applicants.**

The question is about the optimal strategy to maximize the probability of selecting the best applicant.

If the decison can be deferred to the end,this can be solved by the simple maximum selection algotithm of traking the running maximum,and selecting the overall maximum at the end.The difficulty is that the decision must be made immediately.

The mathematical principle--Optimal Stopping Theory
--
The probability of win using is:

Our idea is we choose r which we can use the first element better than it,than we think the element is best chioce.So,now we have a question,if the turly best element is before K,we can not find the best,the probability is 0,if not,we have:

$$\begin{equation}\begin{split} 
P_{r}&=\sum_{k=r}^n P(K^{th}\ appliant\ is\ best\ and\ selected)\\
&=\sum_{k=r}^{n} P(K^{th}\ appliant\ is\ best)P(K^{th}\ appliant\ is\ selected\vert it\ is\ best)\\
&=\sum_{k=r}^n \frac {1}{n} P(best\ of\ first\ K-1\ appears\ before\ stage\ r)\\
&=\sum_{k=r}^n \frac {1}{n}\cdot\frac {r-1}{k-1}\\
&=\frac {r-1}{n}\sum_{k=r}^n\frac {1}{k-1}
\end{split}\end{equation}
$$

Now we can make:

$$\begin{equation}\begin{split} 
&\frac {r-1}{n}\sum_{k=r}^n\frac {1}{k-1}\\
&\approx \frac {r}{n}\int_{r}^{n}\frac {1}{k}dk\\
&=\frac {r}{n}ln\frac {n}{r}
\end{split}\end{equation}
$$

Let $$g(x)=\frac {x}{n}ln\frac {n}{x}$$,and we can get $$g'(x)=\frac {1}{n}ln\frac {n}{x}-\frac {1}{n}$$.

Now we find the max value of this function,we have:

$$g'(x)=0 \Rightarrow ln\frac {n}{x}=1 \Rightarrow x=\frac {n}{e}$$

So,now we know the $$r=\frac {n}{e}$$,and the probability that we find the max of $$n$$ is $$\frac {1}{e}$$.

Dynamic programming
--
I will give its solution in next paper.i am tried now,zZZ.

**References:**
--

1,[Chapter 2. FINITE HORIZON PROBLEMS.](http://www.math.ucla.edu/~tom/Stopping/sr2.pdf)

2,[Secretary problem](https://en.wikipedia.org/wiki/Secretary_problem)

3,[SUM THE ODDS TO ONE AND STOP](https://projecteuclid.org/download/pdf_1/euclid.aop/1019160340)

4,[实用马尔可夫决策过程](https://books.google.com.hk/books?id=iAan6NMMAzcC&pg=PR33&lpg=PR33&dq=动态规划+秘书问题&source=bl&ots=uKSm_c-q1X&sig=0WLQRS0PifOQdSypIul_M5HKflM&hl=zh-CN&sa=X&redir_esc=y#v=onepage&q=动态规划%20秘书问题&f=false)
