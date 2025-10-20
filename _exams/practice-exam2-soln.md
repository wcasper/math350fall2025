---
layout: page
title: Practice Exam 2 Solutions
permalink: /exams/practice-exam2-soln
---

Solve each of the following problems.
If the problem asks for a proof, be sure to carefully justify your work, including any theorems from class.

Note: you may NOT use a theorem or result from class to prove something when it makes the problem entirely trivial.  If you are unsure whether a particular theorem or result is allowed, just ask!

## Problem 1 (True or False)
For each of the following, write TRUE if the statement is true and FALSE if the statement is false.  NO explanation is needed.
Assume both $$(s_n)$$ and $$(t_n)$$ are sequences of real numbers.

a) In a metric space $$M$$ with the discrete metric, every subset is both open and closed

b) The union of any family of closed sets is closed

c) Every open subset of $$\mathbb{R}$$ with the Euclidean metric is a countable union of disjoint open intervals

d) A convergent sequence must be bounded

e) Every accumulation point is also an adherent point

**Solution:**

T, F, T, T, T

## Problem 2

a) Write down the definition of $$\{x_n\}$$ being a Cauchy sequence and the definition of $$\{x_n\}$$ converging to $$L$$.

b) State the definition of an open cover of a set

c) Carefully state the Heine-Borel Theorem, Bolzano-Weierstrass Theorem, Cantor Intersection Theorem, and Lindelof's Theorem.

**Solution:**

a) A sequence is called Cauchy if for all $$\epsilon > 0$$ there exists an integer $$N>0$$ with 

$$m,n\geq N\quad\Rightarrow\quad d(x_m,x_n) < \epsilon.$$

The sequence converging to $$L$$ means that for all $$\epsilon > 0$$ there exists an integer $$N>0$$ with

$$n\geq N\quad\Rightarrow\quad d(x_n,L) < \epsilon.$$

b) 

An open cover of a set $$A$$ is a family of sets $$\{U_i: i\in I\}$$ such that $$U_i$$ is open for all $$i\in I$$ and $$A\subseteq\bigcup_{i\in I} U_i$$

c) Look them up in the lecture slides

## Problem 3

a) Write down the definition of a metric space.

b) Carefully prove that in a metric space $$(M,d)$$, the open ball 

$$B_M(x;r) = \{y\in M: d(x,y) < r\}$$

is an open set.

**Solution:**

a) A metric space is a pair $$(M,d)$$ consisting of a set $$M$$ and a function $$d: M\times M\rightarrow\mathbb R$$ with the following properties:
* $$d(x,x) = 0$$ for all $$x\in M$$
* (positivity) $$d(x,y)> 0$$ for all $$x,y\in M$$ with $$x\neq y$$
* (symmetry) $$d(x,y) = d(y,x)$$ for all $$x,y\in M$$
* (triangle inequality) $$d(x,y)\leq d(x,z) + d(z,y)$$ for all $$x,y,z\in M$$

b) 
Let $$x\in M$$ and $$r>0$$.
To show that $$B_M(x;r)$$ is open, we need to show that all of its points are interior points.
Let $$y\in B_M(x; r)$$ and take $$s = r-d(x,y) > 0$$.
Then for $$z\in B_M(y,s)$$ we have by symmetry and the triangle inequality

$$d(z,x)\leq d(z,y) + d(y,x) < s + d(y,x) = r - d(x,y) + d(y,x) = r.$$

Therefore $$z\in B_M(x; r)$$.  Since $$z\in B_M(x; r)$$ was arbitrary, this proves $$B_M(y; s)\subseteq B_M(x;r)$$.
Thus $$y$$ is an interior point of $$B_M(x;r)$$ and since $$y\in B_M(x;r)$$ was arbitrary, this proves that $$B_M(x;r)$$ is open.

## Problem 4

a) Write down the definition of a complete metric space.

b) Prove that the space $(0,1]$ with the Euclidean metric is not complete.

c) Prove that the space $\mathbb Z$ with the Euclidean metric is complete.

**Solution:**

a) A metric space $$(M,d)$$ is called complete if any Cauchy sequence in $$M$$ coverges in $$M$$.

b) Consider the sequence $$\{x_n\}$$ defined by $$x_n = 1/n$$.  Then $$x_n$$ converges to $$0$$ in $$\mathbb R$$ with the Euclidean metric.  Since convergent sequences are always Cauchy, this also implies that it is a Cauchy sequence.  However, since $$0$$ is not in the subspace $$(0,1]$$, we get that $$\{x_n\}$$ does not converge in $$(0,1]$$.
Therefore not every Cauchy sequence in $$(0,1]$$ converges in $$(0,1]$$ and this proves the space is not complete.

c) Suppose that $$\{x_n\}$$ is a Cauchy sequence in $$\mathbb Z$$.
Then for all $$\epsilon > 0$$ there exists a positive integer $$N$$ with $$m,n\geq N$$ implying that $$|x_m-x_n| < \epsilon.$$

Now specifically take $$\epsilon = 1/2$$.
Then there exists a positive integer $$N$$ with $$m,n\geq N$$ implying that $$|x_m-x_n| < 1/2.$$
However, if the distance between two integers is less than $$1$$, then it must be the same integer!
This means that for all $$n\geq N$$ we have $$x_n=x_N$$.

We claim that $$\lim_{n\rightarrow\infty} x_n = x_N$$.
To prove this, let $$\epsilon > 0$$ (not nec. $$1/2$$).
Then for any $$n\geq N$$, we have

$$d(x_n,x_N) = 0 < \epsilon.$$

Since $$\epsilon > 0$$ was arbitrary ,this proves that $$\lim_{n\rightarrow\infty} x_n = x_N$$.


## Problem 5

a) Let $$(S,d_S)$$ and $$(T,d_T)$$ be metric spaces and $$A\subseteq S$$.  If $$a\in S$$ is accumulation point of $$A$$ and $$f: A\rightarrow T$$ is a function, write the definition of $$\lim_{x\rightarrow a} f(x) = L$$.

b) Let $$f: \mathbb{R}^2\rightarrow\mathbb{R}$$ be the function defined by

$$f(x,y) = \left\lbrace\begin{array}{cc}
(x+y)\sin(1/x)\sin(1/y), &  (x,y)\neq (0,0)\\
0, & x =0\ \text{or}\ y=0
\end{array}\right.$$

Does the limit

$$\lim_{(x,y)\rightarrow (0,0)} f(x,y)$$

exist?  Carefully explain.

**Solution:**

a)  For all $$\epsilon > 0$$ there exists $$\delta > 0$$ such that 

$$0 < d_S(x,a) < \delta\Rightarrow d_T(f(x),L) < \epsilon.$$

b) We claim

$$\lim_{(x,y)\rightarrow(0,0)} f(x,y) = 0.$$

To see this, let $$\epsilon > 0$$.  
Choose $$\delta = \epsilon/2$$.  Then for $$0 < d((x,y),(0,0)) < \delta$ we have

$$0 < \sqrt{x^2 + y^2} < \delta$$

and therefore

$$\begin{align*}
d(f(x,y),0) 
  & = \lvert f(x,y)\rvert\\
  & \leq \lvert (x+y)\sin(1/x)\sin(1/y)\rvert\\
  & \leq \lvert (x+y)\rvert\\
  & \leq \lvert x \rvert + \lvert y\rvert \leq 2\sqrt{x^2 + y^2} < 2\delta = \epsilon.$$
\end{align*}$$

Since $$\epsilon > 0$$ was arbitrary, this proves the stated limit.

## Problem 6

a) Write down the definition of a subset $$S\subseteq M$$ of a metric space $$(M,d)$$ being compact

b) Let $$M=\mathbb{R}$$ with the Euclidean metric.  Prove that the half-open interval $(0,1]$ is not compact directly from the definitions, ie. without using the Heine-Borel Theorem.

**Solution:**

a) That means that every open cover of $$S$$ has a finite subcover.

b) Consider the family of sets $$\{U_i: i\in I\}$$ with index set $$I=\mathbb Z_+$$ and $$U_i = (1/i, 2)$$.

Since each $$U_i$$ is an open interval (a one-dimensional open ball) it is open.
Moreover,

$$\bigcup_{i\in I} U_i = (0,2)\supseteq (0,1],$$

and therefore $$\{U_i: i\in I\}$$ is an open cover of $$(0,1]$$.

To complete our solution, we need to show that it doesn't have any finite subcover.
To see this, consider an arbitrary subfamily

$$\{U_{i_1},U_{i_2},\dots,U_{i_n}\}.$$

Without loss of generality, we may assume $$i_1 < i_2 < \dots < i_n$$.
Noting that the $$U_i$$'s are nested, ie. $$U_1\subseteq U_2\subseteq \dots$$, we get that

$$\bigcup_{k=1}^n U_{i_k} = U_{i_n} = (1/i_n,2).$$

However, $$(0,1]$$ is not a subset of $$(1/i_n,2)$$, so $$\{U_{i_1},U_{i_2},\dots,U_{i_n}\}$$ doesn't cover $$(0,1]$$.
Therefore no finite subfamily will every cover $$(0,1]$$, meaning we won't have a finite subcover.


## Problem 7

Let $$M=\mathbb{R}$$ with the Euclidean metric and consider the subspace

$$S = \{0\}\cup \{\frac{1}{n}: n\in\mathbb{Z}_+\}.$$

a) Show that if $$x\in S$$ is nonzero, then the singleton set $$\{x\}$$ is open in the subspace $$S$$.

b) Show that the singleton set $$\{0\}$$ is not open in $$S$$

BONUS PRACTICE: is $$S$$ a compact metric space?  Why or why not?

**Solution:**

a) If $$x\in S$$ is nonzero, then there exists $$n\in \mathbb Z_+$$ with $$x = 1/n$$.
Take 

$$r = \frac{1}{n} - \frac{1}{n+1} = \frac{1}{n^2+n}$$

to be the distance from $$x$$ to the next closest point in $$S$$.

Then $$(x-r,x+r)$$ is open in $$\mathbb R$$, so

$$(x-r,x+r)\cap S = \{1/n\}$$

is open in the subspace.

b) By way of contradiction, assume $$\{0\}$$ is an open subset of $$S$$.  Then all of its points must be interior points.  By definition, this would mean that there should exist an $$r>0$$ with $$B_S(0;r)\subseteq\{0\}$$.  However, we can choose $$n>1/r$$ so that $$1/n < r$$.
This impiles that 

$$B_S(0; r) = B(0; r)\cap S = (-r,r)\cap S$$

contains $$1/n$$.  This contradicts $$B_S(0;r)\subseteq\{0\}$$.  Therefore $$\{0\}$$ is not open.

BONUS: The set $$S$$ is closed and bounded, so by Heine-Borel it is compact.

## Problem 8

Suppose that $$\{x_n\}$$ is a monotone decreasing sequence of real numbers which is bounded below.

a) Show that using the Euclidean metric, $$\{x_n\}$$ will converge (without using the Monotone Convergence Theorem!)

b) Give an example showing that under the discrete metric, $$\{x_n\}$$ actually might not converge

**Solution:**

a) Let

$$X = \{x_1,x_2,x_3,\dots\}.$$

By the Completeness Axiom, there exists $$a=\inf(X)$$.
We claim that $$\lim_{n\rightarrow\infty} x_n = a$$.
To see this, let $$\epsilon > 0$$.
Then by the definition of an infimum, $$a+\epsilon$$ cannot be a lower bound of $$X$$.
This means that there exists $$x\in X$$ with $$x < a+\epsilon$$.
Moreover, $$x=x_N$$ for some integer $$N\in\mathbb Z_+$$.
Then for any $$n\geq N$$ the fact that the sequence is monotone decreasing implies $$x_n\leq x_N$$ and therefore

$$a \leq x_n\leq x_N < a + \epsilon.$$

It follows that for all $$n\geq N$$

$$\lvert x_n-a\rvert\leq \lvert x_N-a\rvert <\epsilon.$$

Since $$\epsilon > 0$$ was arbitrary, this proves $$\lim_{n\rightarrow\infty} x_n = a.$$

b) The sequence $$\{x_n\}$$ defined by $$x_n = 1/n$$ is monotone decreasing and bounded below by $$0$$.
However, for $$d$$ the discrete metric, $$d(x_m,x_n)=1$$ for all $$m\neq n$$.  This tells us that the sequence is not Cauchy!  Since convergent sequences are Cauchy, we conclclude that the sequence doesn't converge if we are using the discrete metric.



