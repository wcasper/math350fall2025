---
layout: page
title: Homework 7
permalink: /homework/hw7
---

### Directions
Solve the following problems and write up your solutions.  Your solutions should be provided in one of the following formats (in order of preference)
* typed up in $$\LaTeX$$ and submitted as a PDF on Canvas
* written legibly on blank paper, scanned into a PDF and then uploaded on Canvas
* written on ancient parchement with a quill and then flown to the instructor via owl post like in Harry Potter

If you go with the first strategy, you may wish to check out Overleaf which is a free and intuitive website for generating $$\LaTeX$$ documents online.
If you wish to use the second method and don't own a scanner at home, you can check out the numerous scanning apps available for smartphones.

You will be graded based on *completion* of all of the assigned problems, along with in-depth grading of *select* problems which will not be revealed until after the homework is graded.

**Remember:** Success in any math class is based on *practice*.  The assigned homework problems are the **bare minimum**.  You should strive to do as many problems as possible from the textbook.

**Note:** All sets will be subsets of $$\mathbb R$$ unless otherwise stated.

### Problems

**Problem 1:**

Let $$\epsilon > 0$$.
For each of the following choices of $$a$$, $$b$$, $$f(x)$$, find a partition $$P_\epsilon$$ with the specified number $$n$$ of rectangles satisfying 

$$P_\epsilon\subseteq P\ \ \Rightarrow\ \ \lvert R(P,f,\{t_k\})- A\rvert < \epsilon$$

where here $$A = \int_a^b f(x) dx$$.

* (a) $$n=3$$, $$a=1$$, $$b=3$$, and 

$$f(x) = \left\lbrace\begin{array}{cc}
1 & x < 2\\
3 & x\geq 2
\end{array}\right.$$

* (b) $$n=3$$, $$a=1$$, $$b=3$$, and 

$$f(x) = \left\lbrace\begin{array}{cc}
1 & x\leq 2\\
3 & x > 2
\end{array}\right.$$

* (c) $$n=4$$, $$a=1$$, $$b=3$$, and 

$$f(x) = \left\lbrace\begin{array}{cc}
1 & x < 2\\
2 & x = 2\\
3 & x > 2
\end{array}\right.$$

**Problem 2:**

Suppose that $$f(x)$$ is a function which is continuous at $$x=c$$ and let

$$\alpha(x) = \left\lbrace\begin{array}{cc}
0 & x < c\\
1 & x\geq c
\end{array}\right.$$

Prove that if $$c\in (a,b)$$ then

$$\int_a^b f d\alpha = f(c).$$

**Problem 3:** 

Consider the Dirichlet function

$$f(x) = \left\lbrace\begin{array}{cc}
1 & x \in\mathbb Q\\
0 & x \notin \mathbb Q
\end{array}\right.$$

* (a) Prove that every left and right Riemann sum of $$f(x)$$ on $$[0,1]$$ with equally spaced rectangles is equal to $$1$$
* (b) Prove that $$f(x)$$ is not Riemann integrable on $$[0,1]$$


**Problem 4:**

Prove that the function

$$f(x) = \left\lbrace\begin{array}{cc}
0 & x=1/n,\ \ n\in\mathbb Z_+\\
1 & x \text{otherwise}
\end{array}\right.$$

is Riemann integrable on $$[0,1]$$ and calculate $$\int_0^1 f(x) dx$$.

**Problem 5:**

Calculate the upper and lower Riemann-Stieltjes integrals of $$f(x) = x^2$$ on the interval $$[1,3]$$ and prove that $$f(x)$$ is Riemann integrable on $$[1,3]$$.


