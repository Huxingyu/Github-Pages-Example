---
layout: post
title: The Mathematical Basis Of Convex Optimization
description: Some knowledge of matrix theory and real analysis.
category: blog
---

This winter vacation i'm trying to understand this course--Convex Optimization,with current paper.I want make some contribution to some open problems in the field of communicaton optimization.

This will be a series of articles,where i only give the most basic mathematical concepts,the other will be separate article.

Reference material:

- Convex Optimization -by Stephen Boyd
- PKU Course-00136660 Lecture

Lines and line segements
--
Suppose $$x_1\neq x_2$$ are two points in $$R^n$$,Point of form
$$ y=\theta x1+(1-\theta)x2,\theta \in R$$
form the line passing through $$x_1$$ and $$x_2$$.

Values of the parameter \theta between 0 and 1 correspond to the (closed) line segement between $$x1$$ and $$x2$$.

![line](/images/convex/basic/line.JPG)

Affine sets
--
A set $$C \subseteq R^n$$ is affine if the line through any two distinct points in $$C$$ lies in $$C$$.

If for any $$x_1$$,$$x_2 \in C$$ and $$\theta \in R$$,we have $$\theta x_1 + (1 - \theta)x_2 \in C$$.In other word,$$C$$ contains the linear combination of any two points in $$C$$,which sum to one.

The idea can be generalized to more than points.We refer to a point of the form $$\theta_1 x_1+\ldots +\theta_kx_k$$,where $$\theta_1 x_1+\ldots +\theta_kx_k = 1$$,as an affine combination of the points $$x_1,\ldots,x_k$$.

Using induction from the definition of affine set $$i.e$$ that it contain every affine combination of two points in it,it can be shown that an affine set contain every affine combination of its points.If C is an affine set,$$x_1,\ldots,x_k \in C$$,and $$\theta_1 x_1+\ldots +\theta_kx_k = 1$$,then the point $$\theta_1 x_1+\ldots +\theta_kx_k$$ also belong to $$C$$.

..etc(i will write it in nextday)








