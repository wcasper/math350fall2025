---
layout: page
title: Practice Final Solutions
permalink: /exams/practice-final-soln
---

Solve each of the following problems.
If the problem asks for a proof, be sure to carefully justify your work, including any theorems from class.

Note: you may NOT use a theorem or result from class to prove something when it makes the problem entirely trivial.  If you are unsure whether a particular theorem or result is allowed, just ask!

## Problem 1

Prove that the positive integers are not bounded above using first principles.
Do not use the Archimedian Principle.

**Solution:**

Suppose that $$\mathbb Z_+$$ is bounded above.
Then by the Completeness Axiom, it has a sumpremum $$x$$.
Remember this means
* $$x$$ is an upper bound of $$\mathbb Z_+$$ and
* anything less than $$x$$ is NOT an upper bound of $$\mathbb Z_+$$
By the definition of a supremum, the element $$x-1$$ cannot be an upper bound of $$\mathbb Z_+$$.
Therefore there exists $$n\in\mathbb Z_+$$ with $$n>x-1$$.
However, if $$n\in\mathbb Z_+$$ then $$n+1$$ is also in $$\mathbb Z_+$$ and 

$$n+1 > (x-1) + 1 = x.$$

This shows that $$x$$ is not an upper bound of $$\mathbb Z_+$$.
This is a contradition.

## Problem 2

Let $$(S,d_S)$$ and $$(T,d_T)$$ be metric spaces and suppose $$f: S\rightarrow T$$ is continuous.

* (a) Prove that if $$K\subseteq S$$ is compact, then $$f(K)$$ is compact.
* (b) Prove that if $$S$$ is compact, then for every closed set $$C\subseteq S$$ the image $$f(C)$$ is closed.
* (c) Give an example of a non-compact $$S$$ and closed subset $$C\subseteq S$$ with $$f(C)$$ not closed.

**Solution:**

* (a) Let $$\{V_i: i\in I\}$$ be an open cover of $$f(K)$$.
Since $$f$$ is continuous, the set $$U_i = f^{-1}(V_i)$$ is open in $$S$$ for all $$i\in I$$.
Furthermore,

$$f(K)\subseteq \bigcup_{i\in I} V_i,$$

and therefore
$$K\subseteq f^{-1}(f(K))\subseteq f^{-1}\left(\bigcup_{i\in I} V_i\right) = \bigcup_{i\in I} f^{-1}(V_i) = \bigcup_{i\in I} U_i.$$

Thus $$\{U_i: i\in I\}$$ is an open cover of $$K$$.
Since $$K$$ is compact, it must have a finite subcover $$\{U_{i_1},\dots, U_{i_r}\}$$.
This means

$$K\subseteq\bigcup_{k=1}^r U_{i_k}$$

and therefore

$$f(K)\subseteq f\left(\bigcup_{k=1}^r U_{i_k}\right) = \bigcup_{k=1}^r f(U_{i_k}) = \bigcup_{k=1}^r f(f^{-1}(V_{i_k}))\subseteq \bigcup_{k=1}^r V_{i_k}.$$

Thus $$\{V_{i_1},\dots, V_{i_r}\}$$ covers $$f(K)$$ and is a finite subcover of $$\{V_i: i\in I\}$$.
Since we started with an arbitrary open cover of $$f(K)$$, this proves that $$f(K)$$ is compact.

## Problem 3

Let $$f(x) = 2x$$ and

$$\alpha(x) = 
\left\lbrace\begin{array}{cc}
x-1 & 0 \leq x < 1/2\\
x+1 & 1/2 \leq x \leq 1\\
\end{array}\right.$$

Show that $$f$$ is integrable with respect to $$\alpha$$ on $$[0,1]$$ and calculate the Riemann-Stieltjes integral $$\int_0^1fd\alpha.$$
Carefully justify all steps.

**Solution:**

Let $$n>0$$ be an integer and consider the partition

$$P = \left\lbrace\frac{0}{2n},\frac{1}{2n},\dots,\frac{n}{2n},\dots,\frac{2n}{2n}\right\rbrace.$$

The upper Stieltjes sum is

$$\begin{align}
\overline S(P,f,\alpha)
  & = \sum_{k=1}^{2n} M_k (\alpha(x_k)-\alpha(x_{k-1}))\\
  & = \sum_{k=1}^{n-1} M_k (\alpha(x_k)-\alpha(x_{k-1})) + M_n (\alpha(x_n)-\alpha(x_{n-1})) + \sum_{k=n+1}^{2n} M_k (\alpha(x_k)-\alpha(x_{k-1}))\\
  & = \sum_{k=1}^{n-1} M_k \frac{1}{2n} + M_n \left(\frac{1}{2n} + 2\right) + \sum_{k=n+1}^{2n} M_k \frac{1}{2n}\\
  & = \sum_{k=1}^{2n} M_k \frac{1}{2n}  + 2M_n \\
  & = \sum_{k=1}^{2n} 2\frac{k}{2n} \frac{1}{2n}  + 2\frac{n}{2n} \\
  & = \frac{1}{2n^2}\sum_{k=1}^{2n} k  + 1 \\
  & = \frac{1}{2n^2}\frac{2n(2n+1)}{2}  + 1 = 2 + \frac{1}{2n}
\end{align}$$

The lower Stieltjes sum is

$$\begin{align}
\overline S(P,f,\alpha)
  & = \sum_{k=1}^{2n} m_k (\alpha(x_k)-\alpha(x_{k-1}))\\
  & = \sum_{k=1}^{n-1} m_k (\alpha(x_k)-\alpha(x_{k-1})) + m_n (\alpha(x_n)-\alpha(x_{n-1})) + \sum_{k=n+1}^{2n} m_k (\alpha(x_k)-\alpha(x_{k-1}))\\
  & = \sum_{k=1}^{n-1} m_k \frac{1}{2n} + m_n \left(\frac{1}{2n} + 2\right) + \sum_{k=n+1}^{2n} m_k \frac{1}{2n}\\
  & = \sum_{k=1}^{2n} m_k \frac{1}{2n}  + 2m_n \\
  & = \sum_{k=1}^{2n} 2\frac{k-1}{2n} \frac{1}{2n}  + 2\frac{n-1}{2n} \\
  & = \frac{1}{2n^2}\sum_{k=1}^{2n} (k-1)  + 1 - \frac{1}{n} \\
  & = \frac{1}{2n^2}\frac{2n(2n-1)}{2}  + 1 - \frac{1}{n} = 2 - \frac{3}{2n}
\end{align}$$

Therefore

$$2 - \frac{3}{2n}\leq \underline{\int}_0^1 fd\alpha \leq \overline{\int}_0^1 fd\alpha \leq \overline S(P,f,\alpha) = 2 +\frac{1}{2n}.$$

Since $$n$$ was an arbitrary positive integer, we can take the limit as $$n\rightarrow\infty$$ and get

$$2\leq \underline{\int}_0^1 fd\alpha \leq \overline{\int}_0^1 fd\alpha \leq 2.$$

Therefore the upper and lower Stieltjes integrals are equal, forcing the function to be integrable and

$$\underline{\int}_0^1 fd\alpha = \overline{\int}_0^1 fd\alpha = \int_0^1 fd\alpha = 2.$$

## Problem 4

Let $$(M,d)$$ be a metric space, and suppose that there is a sequence $$\{x_n\}$$ of elements of $$M$$ and a value $$L$$ in $$M$$ with the following property.
* Every subsequence of $$\{x_n\}$$ has a further subsequence which converges to $$L$$.
Prove that $$\{x_n\}$$ must converge to $$L$$.

**Solution:**

Suppose that $$\{x_n\}$ does NOT converge to $$L$$.
Then there exists $$\epsilon > 0$$ such that for all $$N$$ there is an $$n\geq N$$ with $$d(x_n,L) \geq\epsilon$$.

Choose $$n_1$$ with $$d(x_{n_1},L) \geq\epsilon$$.
Next, choose $$n_2\geq n_1+1$$ with $$d(x_{n_2},L)\geq \epsilon$$.
In fact, in for each $$k\geq 2$$, choose $$n_{k+1}\geq n_k+1$$ with $$d(x_{n_{k+1}},L)\geq \epsilon$$.

Then $$\{x_{n_k}\}$$ is a subsequence of $$\{x_n\}$$ with the property that $$d(x_{n_k},L)\geq \epsilon$$ for all integers $$k\geq 1$$.
By the statement of the problem, $$\{x_{n_k}\}$$ should have a further subsequence which converges to $$j$$.
This would imply that $$L$$ is an accumulation point of the set

$$X = \{x_{n_k}: k\in\mathbb{N}\}.$$

However, the ball of radius epxilon around $L$ satisfies $$B_M(L,\epsilon)\cap X = \varnothing$$.
This is a contradiction.

## Problem 5

For each of the following choices of $$S$$ and $$T$$, give an example of a continuous, surjective function $$f: S\rightarrow T$$ or explain why no such example exists.
Note all metrics are Euclidean.

* (a) $$S = (0,1)$$ and $$T=(0,1]$$
* (b) $$S = (0,1)$$ and $$T=(0,1)\cup(1,2)$$
* (c) $$S = [0,1]\cup [2,3]$$ and $$T = \{0,1\}$$
* (d) $$S = \mathbb{R}$$ and $$T = \mathbb{Q}$$
* (e) $$S = [0,1]\times [0,1]\subseteq \mathbb{R}^2$$ and $$T = (0,1)\times (0,1)\subseteq\mathbb R^2$$

* (a) Take $$f(x) = 1-(2x-1)^2$$.
* (b) Impossible, since the continuous image of a connected set is connected
* (c) Take $$f = \left\lbrace\begin{array}{cc}0, & 0\leq x\leq 1\\1, & 2\leq x\leq 3\end{array}\right.$$
* (d) Impossible, since the continuous image of a connected set is connected, and $$\mathbb{R}$$ Is connected, but $$\mathbb{Q}$$ is disconnected
* (e) Impossible, since the continuous image of a compact set is compact.  $$S$$ is compact since it is closed and bounded (Heine-Borel), but $$T$$ is not compact since it is not closed.

## Problem 6

Suppose that $$f$$ is a real-valued function on $$\mathbb{R}$$ which is twice differentiable at $$x=c$$.
Define a new function

$$g(x) = \left\lbrace\begin{array}{cc}
\frac{f(x)-f(c)}{x-c}, & x\neq c\\
f'(c), & x = c\\
\end{array}\right.$$

Show that $$g$$ is differentiable at $$x=c$$ and that $$g'(c) = \frac{1}{2}f''(c)$$.

**Solution:**

By the Helper Theorem, the fact that $$f(x)$$ is differentiable at $$x=c$$ implies that there is a function $$f^*(x)$$ which is continuous at $$x=c$$ with $$f^*(c) = f'(c)$$ and

$$f(x)-f(c) = (x-c)f^*(x).$$

Furthermore, since $$f$$ is twice differentiable, the function $$f^*(x)$$ is differentiable at $$x=c$$.
Taking the second derivative of both sides at $$x=$$ and using the product rule twice:

$$f''(c) = 2f^{*'}(c).$$

Hence

$$\lim_{x\rightarrow c}\frac{g(x)-g(c)}{x-c} = \lim_{x\rightarrow c}\frac{f(x)-f(c)-(x-c)f'(c)}{(x-c)^2} = \lim_{x\rightarrow c}\frac{f^*(x)-f'(c)}{(x-c)} = f^{*'}(c) = \frac{1}{2}f''(c).$$



## Problem 7

* (a) State the Mean Value Theorem
* (b) State the Intermediate Value Theorem
* (c) Prove that the polynomial $$x^{2023} + x^{15} + 3x^5 + 2x - 6$$ has exactly one real root, and that this root must lie in the interval $$(0,1)$$.

* (a) Look it up
* (b) Look it up
* (c) The polynomial $$f(x) =x^{2023} + x^{15} + 3x^5 + 2x - 6$$ is continuous on $$[0,1]$$ and differentiable on $$(0,1)$$.
It satisfies $$f(0) = -6$$ and $$f(1) = 1$$, so by the IVT, there exists a value of $$a\in (0,1)$$ with $$f(a) = 0$$.
In particular $$f(x)$$ has a root on the interval $$(0,1)$$.
Now suppose $$f(x)$$ had another root at a point $$b\in\mathbb{R}$$ different from $$a$$.
Then $$f(a) =0$$ and $$f(b) = 0$$, so by the Mean Value Theorem, there must exist a $$c$$ between $$a$$ and $$b$$ with

$$f'(c) = \frac{f(b)-f(a)}{b-a} = 0.$$

However,

$$f'(x) = 2023x^{2022} + 15x^{14} + 15x^4 + 2$$

is the sum of four positive numbers, so it can never be zero!  Thus $$f$$ cannot have more than one root.




