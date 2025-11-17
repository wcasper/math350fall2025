---
layout: page
title: Practice Exam 3 Solutions
permalink: /exams/practice-exam3-soln
---

Solve each of the following problems.
If the problem asks for a proof, be sure to carefully justify your work, including any theorems from class.

Note: you may NOT use a theorem or result from class to prove something when it makes the problem entirely trivial.  If you are unsure whether a particular theorem or result is allowed, just ask!

## Problem 1 (True or False)
For each of the following, write TRUE if the statement is true and FALSE if the statement is false.  NO explanation is needed.
Assume both $$(s_n)$$ and $$(t_n)$$ are sequences of real numbers.

a) If $$f: [0,1]\rightarrow (0,2]$$ is surjective, then it cannot be continuous.

b) If $$f: \mathbb{R}\rightarrow \{x\in\mathbb{R}: x\neq 0\}$$ is surjective, then it cannot be continuous.

c) The series $$\sum_{n=1}^\infty \frac{1}{n}$$ converges

d) A function $$f: [0,1]\rightarrow \mathbb{R}$$ must have an absolute maximum.

e) If $$f: \mathbb{R}\rightarrow\mathbb{R}$$ is a continuous function, then the image $$f((0,1)) = \{f(t): 0 < t < 1\}$$ must be open.

**Solution:**

T, T, F, T, F


## Problem 2

a) State the definition of the limit supremum of a sequence $$a_n$$

b) Determine, with proof, the limit supremum of the sequence $$x_n=\cos(n)$$

c) Prove that if $$a_n$$ and $$b_n$$ are positive, bounded sequences then

$$\limsup(a_nb_n) \leq \limsup(a_n)\limsup(b_n)$$

**Solution:**

a) The limit supremum is 

$$\limsup a_n = \lim_{n\rightarrow\infty} M_n$$

where here

$$M_n = \sup\{a_n, a_{n+1}, a_{n+2}, a_{n+3},\dots\}.$$

b)  We claim that the limit supremum is $$1$$.  To prove this, we will show that $$M_n=1$$ for all $$n$$ and therefore $$\lim_{n\rightarrow\infty} M_n = 1$$.

Fix $$n\in\mathbb Z_+$$.
To prove $$M_n=1$$, we must show two things: that $$1$$ is an upper bound of $$\{\cos(k): k\geq n\}$$ and that anything smaller than $$1$$ is not an upper bound.

Since $$\cos(x)\leq 1$$ for all $$x$$, it's clear that $$1$$ is an upper bound.


Let $$1 > \epsilon > 0$$.  We must show that $$1-\epsilon$$ is NOT an upper bound of $$\{\cos(k): k\geq n\}$$.
For each $$k\in\mathbb Z_+$$, define $$m_k=\lfloor 2\pi k\rfloor$$ and $$x_k = 2\pi k-n_k$$.
The set

$$\{x_{nk}: k\in\mathbb Z_+\}$$

is an infinite subset of $$(0,1)$$, so there must exist $$j,k\in\mathbb Z_+$$ with $$j\neq k$$ and $$\lvert x_{nj}-x_{nk}\rvert < \cos^{-1}(1-\epsilon)$$.

Then $$m = \lvert m_{nj}-m_{nk}\rvert$$ is a positive integer multiple of $$n$$, so $$m \geq n$$.  Moreover

$$\cos(m) = \cos(m_{nj}-m_{nk}) = \cos(x_{mj}-x_{nk}) > 1-\epsilon.$$

This shows that $$1-\epsilon$$ is not an upper bound.

c)  Note that this problem doesn't have anything to do with part (b).  Let $$\alpha = \limsup a_n$$ and $$\beta = \limsup b_n$$ and $$c_n =a_nb_n$$.  Since $$a_n$$ and $$b_n$$ are bounded sequences, $$c_n$$ is also a bounded sequence.  This implies that $$\limsup c_n$$ exists.  

Define

$$M_n^a = \sup\{a_k: k\geq n\},\quad M_n^b = \sup\{b_k: k\geq n\},\quad M_n^c = \sup\{c_k: k\geq n\}.$$

If $$k\geq n$$, then $$a_k\leq M_n^a$$ and $$b_k\leq M_n^b$$ and therefore

$$c_k = a_kb_k\leq M_n^aM_n^b.$$

It follows that $$\{c_k: k\geq n\}$$ is bounded above by $$M_n^aM_n^b$$.  Since $$M_n^c$$ is the *least* upper bound, we obtain

$$M_n^c\leq M_n^aM_n^b.$$

Since limits preserve inequalities, and the limit of a product is the product of the limits, it follows that

$$\limsup c_n =\lim M_n^c\leq \lim (M_n^aM_n^b) = (\lim M_n^a)(\lim M_n^b) = (\limsup a_n)(\limsup b_n).$$


## Problem 3

* (a) Let $$(S,d_S)$$ and $$(T,d_T)$$ be metric spaces and $$f: S\rightarrow T$$.  Write down the definition of $$f$$ being continuous at a point $$a\in S$$.
* (b) Prove that the function $$f: \mathbb{R}\rightarrow\mathbb{R}$$ defined by

$$f(x) = \sqrt{x^2 + 1}$$

is continuous at the point $$x=0$$.

**Solution:**

* (a) The function $$f$$ is continuous at $$a\in S$$ if for all $$\epsilon > 0$$ there exists $$\delta > 0$$ such that 

$$d_S(x,a) < \delta\ \ \Rightarrow d_T(f(x),f(a)) < \epsilon\ \ \forall a\in x\in S$$.

* (b) Let $$\epsilon > 0$$.  Choose $$\delta = \sqrt{2\epsilon}.$$

Then for $$\lvert x-0\rvert < \delta$$ we have

$$\lvert f(x) - f(0)\rvert =  \lvert \sqrt{x^2+1}-1\rvert = \frac{x^2}{\sqrt{x^2+1}+1} \leq \frac{x^2}{2} < \frac{\delta^2}{2} = \epsilon.$$

Since $$\epsilon > 0$$ was arbitrary, this proves $$f(x)$$ is continuous at $$x=0$$.

## Problem 4

* a) State the root test for series.

* b) Prove the root test for series.

* c) Explain why the series 

$$\sum_{n=1}^\infty \frac{1}{2^{\lfloor n/2\rfloor}}$$

converges, where here $$\lfloor x\rfloor$$ is the greatest integer less than or equal to $$x$$ (ie. $$x$$ rounded down).


**Solution:**

* (a) Set $$\rho = \limsup \sqrt[n]{\lvert a_n\rvert}.$$  Then 
  - if $$\rho < 1$$ the series $$\sum a_n$$ is absolutely convergent
  - if $$\rho > 1$$ the series $$\sum a_n$$ is divergent
  - if $$\rho = 1$$ the test tells us nothing

* (b) Let 

$$M_n = \sup \{\sqrt[k]{\lvert a_k\rvert}: k\geq n\}$$

Suppose that $$\rho < 1$$.
Then for all $$\epsilon > 0$$ there exists $$N\in\mathbb Z_+$$ such that for $$n\geq N$$ $$\lvert M_n - \rho\rvert < \epsilon.$$

Take $$\epsilon = (1-\rho)/2$$.
Then for all $$n\geq N$$ we know $$M_n < \rho + \epsilon = (1+\rho)/2 < 1.$$
Therefore for all $$n\geq N$$, we have

$$\sqrt[n]{\lvert a_n\rvert} \leq M_N < (1+\rho)/2,$$

so that $$\lvert a_n\rvert < \left(\frac{1+\rho}{2}\right)^n.$$
It follows that for all $$n\geq N$$ the partial sums of the series $$\sum \lvert a_n\rvert$$ satisfy

$$\begin{align*}
s_n
  & = \sum_{k=1}^n\lvert a_k\rvert\\
  & = \sum_{k=1}^N \lvert a_k\rvert + \sum_{k=N+1}^N \lvert a_k\rvert\\
  & < \sum_{k=1}^N \lvert a_k\rvert + \sum_{k=N+1}^N \left(\frac{1+\rho}{2}\right)^k\\
  & < \sum_{k=1}^N \lvert a_k\rvert + \sum_{k=1}^\infty \left(\frac{1+\rho}{2}\right)^k\\
  & = \sum_{k=1}^N \lvert a_k\rvert + \frac{\frac{1+\rho}{2}}{1-\frac{1+\rho}{2}}.
\end{align*}$$

Therefore $$s_k$$ is bounded above.  Since it's also monotone increasing, the Monotone Convergence Theorem tells us $$s_n$$ converges.  Hence $$\sum s_n$$ is absolutely convergent.  Therefore it is convergent.

Now suppose instead that $$\rho > 1$$.
By way of contradiction, assume that $$\sum a_n$$ converges.
Then by the Divergence Test, $$\lim a_n=0$$.
Therefore for all $$\epsilon_1 > 0$$ there exists $$N_1\in\mathbb Z_+$$ such that $$n\geq N$$ implies $$\lvert a_n\rvert <\epsilon_1$$.
Also for all $$\epsilon_2 > 0$$ there exists $$N_2\in\mathbb Z_+$$ such that $$n\geq N$$ implies $$\lvert M_n-\rho\rvert <\epsilon_2$$.

Take $$\epsilon_1 = 1$$ and $$epsilon_2=(\rho-1)/2$$ and set $$N = \max(N_1,N_2)$$.
Then for all $$n\geq N$$ we have $$\lvert a_n\rvert < 1$$ and also

$$M_n > \rho-\epsilon =  \frac{1+\rho}{2} > 1.$$
Therefore by the definition of a supremum, there exists $$k\geq n$$ with $$\sqrt[k]{\lvert a_k\rvert} > 1.$$
Hence $$\lvert a_k\rvert > 1$$.  However, since $$k\geq n\geq N$$, we must have $$\lvert a_k\rvert < 1$$, which is a contradiction.
Therefore the series $$\sum a_n$$ must diverge.

* c) 

In this case,

$$\rho = \limsup \sqrt[n]{\frac{1}{2^{\lfloor n/2\rfloor}}} = \limsup \frac{1}{2^{\lfloor n/2\rfloor}/n}

Let 

$$M_n = \sup\{\frac{1}{2^{\lfloor k/2\rfloor}/k}: k\geq n\}.$$

Then clearly $$M_n \leq \frac{1}{2^{(n-1)/2n}} < \frac{1}{\sqrt{2}}$$, so $$\rho=\lim M_n \leq \frac{1}{\sqrt{2}} < 1.$$

Thus by the root test, the series is absolutely convergent.


## Problem 5

Let $$(S,d_S)$$ and $$(T,d_T)$$ be metric spaces and suppose $$f: S\rightarrow T$$ is continuous.

* (a) Prove that if $$K\subseteq S$$ is compact, then $$f(K)$$ is compact.
* (b) Prove that if $$S$$ is compact, then for every closed set $$C\subseteq S$$ the image $$f(C)$$ is closed.
* (c) Give an example of a non-compact $$S$$ and closed subset $$C\subseteq S$$ with $$f(C)$$ not closed.

**Solution:**

* (a) 

Let $$\{V_i: i\in I\}$$ be an open cover of $$f(K)$$.
For each $$i\in I$$, set $$U_i = f^{-1}(V_i)$$.
Since $$f$$ is continuous $$U_i$$ is open for all $$i$$.

Also since $$f(K)\subseteq \bigcup_{i\in I} V_i$$, we know

$$K \subseteq f^{-1}(f(K))\subseteq f^{-1}\left(\bigcup_{i\in I} V_i\right) = \bigcup_{i\in I} U_i.$$

Therefore $$\{U_i: i\in I\}$$ is an open cover of $$K$$.
It follows that it has a finite subcover

$$\{U_{i_1},U_{i_2},\dots, U_{i_n}\}$$

However, this means

$$f(K)\subseteq f\left(\bigcup_{k=1}^n U_{i_k}\right) = \bigcup_{k=1}^n f(U_{i_k})\subseteq \bigcup_{k=1}^n V_{i_k}.$$

Therefore 

$$\{V_{i_1},V_{i_2},\dots, V_{i_n}\}$$

is a finite subcover of $$f(K)$$.  This proves $$K$$ is compact.

* (b) Suppose that $$S$$ is compact and $$C\subseteq S$$ is closed. Then $$C = C\cap S$$ is compact.  Therefore $$f(C)$$ is compact.  Therefore $$f(C)$$ is closed.

* (c) Let $$f: \mathbb R\rightarrow\mathbb R$$ be the function $$f(x) = \frac{1}{1+x^2}$$.  Then since $$f$$ is a rational function, it is continuous.

Moreover $$\mathbb R$$ is closed but

$$f(\mathbb R) = \{f(x): x\in\mathbb R\} = (0,1]$$

is not closed.

## Problem 6

* (a) Let $$f$$ be a real-valued function on $$(a,b)$$.  Write down what it means for $$f$$ to be differentiable at $$c\in (a,b)$$.
* (b) Write down the Quotient Rule for derivatives.  Make sure to carefully state the required assumptions!
* (c) Prove the quotient rule for derivatives.  You may use the Helper Theorem!

**Solution:**

* (a) We say $$f$$ is differentiable at $$c$$ if $$\lim_{x\rightarrow c} \frac{f(x)-f(c)}{x-c}$$ exists.
* (b) Assume that $$f$$ and $$g$$ are differentiable at $$x=c\in (a,b)$$ with $$g(c)\neq 0$$.  Then $$h(x) = f(x)/g(x)$$ is differentiable at $$x=c$$ with

$$h'(c) = \frac{f'(c)g(c)-f(c)g'(c)}{g(c)^2}.$$

* (c) By the Helper Theorem, there exist functions $$f^*,g^*: (a,b)\mathbb R$$ which are continuous at $$x=c$$ and satisfy

$$f(x)-f(c) = (x-c)f^*(x)\ \ \ \text{and}\ \ \ g(x)-g(c) = (x-c)g^*(x).$$

This means that 

$$\begin{align*}
h(x)-h(c)
  &= \frac{f(x)g(c)-f(c)g(x)}{g(x)g(c)}\\
  &= \frac{f(x)g(c)-f(c)g(c)+f(c)g(c)-f(c)g(x)}{g(x)g(c)}\\
  &= \frac{(f(x)-f(c))g(c)-f(c)(g(x)-g(c))}{g(x)g(c)}\\
  &= (x-c)\frac{f^*(x)g(c)-f(c)g^*(x)}{g(x)g(c)}.
\end{align*}

Note that since $$g(x)$$ is differentiable at $$x=c$$ it is also continuous there.
By Properties of Continuous Functions, the quotient $$h^*(x) = \frac{f^*(x)g(c)-f(c)g^*(x)}{g(x)g(c)}$$ is continuous at $$c$$.
Therefore by the Helper Theorem $$h(x)$$ is differentiable at $$x=c$$ and

$$h'(c) = h^*(c) = \frac{f^*(c)g(c)-f(c)g^*(c)}{g(c)^2} = \frac{f'(c)g(c)-f(c)g'(c)}{g(c)^2}.$$

## Problem 7

Let $$S=\mathbb{R}$$ and $$d_S: S\times S\rightarrow \mathbb{R}$$ be the discrete metric on $$S$$, and let $$T=\mathbb{R}$$ with $$d_T: T\times T\rightarrow \mathbb{R}$$ the Euclidean metric.

* (a) Prove that every subset of $$S$$ is open.
* (b) Prove that *any* function $$f: S\rightarrow T$$ is continuous.

**Solution:**

* (a) Let $$A\subseteq S$$.  Then if $$x\in A$$ the ball $$B_S(x;1) = \{x\}\subseteq A$$.  Therefore every point of $$A$$ is an interior point of $$A$$.  This shows that $$A$$ is open.
* (b) Let $$V\subseteq T$$ be open.  Then $$f^{-1}(V)$$ is open, since every subset of $$S$$ is open.  Since preimages of open sets are open, this proves that $$f$$ is continuous.

## Problem 8

Determine whether the following infinite series or products converge or diverge.
If they converge, then find the exact value.

* (a) $$\prod_{n=2}^\infty \frac{n^2-1}{n^2}$$

* (b) $$\sum_{n=1}^{\infty} \frac{1}{n(n+2)}$$

* (c) $$0.11120252025202520252025\dots$$


* (a) The partial products are

$$p_n = \prod_{k=2}^\infty \frac{k^2-1}{k^2} = \prod_{k=1}^\infty \left(\frac{(k-1)(k+1)}{k^2}\right).$$

This product telescopes, so that

$$p_n = \frac{2}{1}\frac{n+1}{n}.$$

Taking the limit, we get $$\lim_{n\rightarrow\infty} p_n = 2.$$
Since the limit of partial products exists, the infinite product converges and is equal to $$2$$.

* (b) The partial sums are

$$s_n = \sum_{k=1}^n \frac{1}{k(k+2}} = \sum_{k=1}^n \frac{1/2}{k} - \frac{1/2}{k+2}.$$

This sum also telescopes, so that

$$s_n = \frac{1}{2} - \frac{1}{6} + \frac{1}{4}-\frac{1}{8} + \frac{1}{6}-\frac{1}{10} + \dots + \frac{1}{2(n-1)} - \frac{1}{2(n+1)} + \frac{1}{2n} - \frac{1}{2(n+2)}$$

becomes

$$s_n = \frac{1}{2} + \frac{1}{4} - \frac{1}{2(n+1)} - \frac{1}{2(n+2)}.$$

Therefore $$\lim s_n = \frac{1}{2} + \frac{1}{4} = \frac{3}{4}.$$
Thus the series converges and is equal to $$3/4$$.

* (c) We can write

$$0.11120252025202520252025\dots = \frac{111}{1000} + \frac{1}{1000}\sum_{k=1}^\infty \left(\frac{2025}{10000}\right)^k$$

Then using the geometric series

$$\frac{111}{1000} + \frac{1}{1000}\frac{\frac{2025}{10000}}{1-\frac{2025}{10000}} = \frac{887250}{7975000}.$$

Therefore 

$$0.11120252025202520252025\dots  = \frac{887250}{7975000}.$$


