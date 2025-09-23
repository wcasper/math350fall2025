---
layout: page
title: Practice Exam 1 Solutions
permalink: /exams/practice-exam1-soln
---

Solve each of the following problems.
If the problem asks for a proof, be sure to carefully justify your work, including any theorems from class.

Note: you may NOT use a theorem or result from class to prove something when it makes the problem entirely trivial.  If you are unsure whether a particular theorem or result is allowed, just ask!

## Problem 1 (True or False)
For each of the following, write TRUE if the statement is true and FALSE if the statement is false.  NO explanation is needed.
Assume both $$(s_n)$$ and $$(t_n)$$ are sequences of real numbers.

a) The set $$\{\mathbb{Z},\mathbb{R}\}$$ is uncountable.

b) The Well-Ordering Principle says that every set of integers has a minimum element.

c) Any set of real numbers which is bounded above has a maximum

d) The set $$\{(1,2),(2,1),(3,3)\}$$ is a relation from $$\mathbb{Z}$$ to $$\mathbb{R}$$

e) Every accumulation point is also an adherent point

**Solution:**

a) False!  It has only two elements!

b) False!  It needs to be *positive* integers!

c) False!  We have a supremum, but potentially no maximum...

d) True!  Any subset of $\mathbb{Z}\times\mathbb{R}$ is a relation

e) True!  Being an accumulation point is a stronger condition.

## Problem 2

a) Write down the five field axioms, the four order axioms, and the completeness axiom

b) State the definition of a supremum

c) Carefully state the Cauchy-Schwarz inequality.

**Solution:**

a) Make sure to know the other axioms, too!
 * commutativity:  $$x+y = y+x$$ and $$xy=yx$$
 * associativity:  $$(x+y) + z = x + (y+z)$$ and $$(xy)z = x(yz)$$
 * distributivity: $$$x(y + z) = xy + xz$$
 * addive inverses: given $$x,y\in F$$, there exists a unique $$z\in F$$ with $$x=y+z$$
 * multiplicative inverse: given $$x,y\in F$$ with $$y\neq 0$$, there exists a unique $$z\in F$$ with $$x = yz$$

b) What about infimum?  Minimum, maximum?  Know your stuff!

A supremum of a set $$A$$ is an element $$x$$ which is an upper bound of $$A$$, but with the property that if $$y < x$$ then $$y$$ is not an upper bound of $$A$$

c) Do we also know Minkowski's Inequality?  The Triangle Ineqeuality?

The Cauchy-Schwarz inequlity says that if $$x_1,\dots, x_n$$ and $$y_1,\dots, y_n$$ are real numbers then

$$\sum_{k=1}^n x_ky_k \leq \left(\sum_{k=1}^n x_k^2\right)^{1/2}\left(\sum_{k=1}^n y_k^2\right)^{1/2}.$$

## Problem 3

a) Give the definition of an upper bound

b) Is the set

$$\left\lbrace\frac{1}{x^2-3}: x\in\mathbb Q\right\rbrace$$

bounded above?  Carefully justify your answer.

**Solution:**

a) An element $$x$$ is an upper bound of a set $$A$$ if $$a\leq x$$ for all $$a\in A$$.

b) No.  To see this, suppose that it is bounded above by some number $$N$$.
Let $$N > 0$$ be an integer.  Then we may choose a rational number $$x$$ with 

$$\sqrt{3} < x < \sqrt{3 + 1/N}.$$ 

Then $$0 < x^2 - 3 < 1/N$$, so that $$N < \frac{1}{x^2-3}$$.
This is a contradiction.

## Problem 4

a) Write down the definition of an open set in $$\mathbb R^n$$.

b) Prove that an open ball in $$\mathbb R^n$$ is an open set.

**Solution:**

a) A subset $$U\subseteq \mathbb R^n$$ is called open if every point in $$U$$ is an interior point of $$U$$.

b) Let $$\vec a\in\mathbb R^n$$ and $$r> 0$$.  We need to prove $$B(\vec a; r)$$ is an open set in $$\mathbb R^n$$, ie. that all of its points are interior points.

Let $$\vec x\in B(\vec a;r)$$.
Then $$\lvert \vec x-\vec a\rvert < r$$ so $$s = r - \lvert \vec x-\vec a\rvert > 0$$.
Furthermore if $$\vec y\in B(\vec x;s)$$ then

$$
\begin{align*}
\lvert \vec y-\vec a\rvert
 & =  \lvert \vec y-\vec x+\vec x-\vec a\rvert\\
 &\leq  \lvert \vec y-\vec x\rvert +\lvert \vec x-\vec a\rvert\\
 &<  s +\lvert \vec x-\vec a\rvert = r.
\end{align*}$$

Therefore $$\vec y\in B(\vec a;r)$$.  Since $$\vec y\in B(\vec x; s)$$ was arbitrary, this proves $$B(\vec x;s)\subseteq B(\vec a;r)$$.
Therefore $$\vec x$$ is an interior point of $$B(\vec a;r)$$.
Since $$\vec x\in B(\vec a; r)$$ was arbitrary, this proves $$B(\vec a; r)$$ is open.

## Problem 5

Consider the relation from $$\mathbb{Z}$$ to $$\mathbb{Z}_+$$ defined by

$$\mathcal R = \{(x+y,xy^2): x\in\mathbb{Z}_+,\ \ y\in\mathbb{Z}\},$$

a) Write what it means for a relation $$\mathcal R$$ from a set $$A$$ to a set $$B$$ to be a function

b) Is $$f(x)$$ a function?  Carefully explain.

**Solution:**

a) For every $$x$$ in the domain of $$\mathcal R$$ there exists a unique $$y$$ with $$x\mathcal R y$$

b) No, since if we take $$x=2$$ and $$y=-2$$ we get the point $$(0,8)$$, but if we take $$x=1$$ and $$y=-1$$ we get the poinit $$(0,1)$$.
Therefore $$0\mathcal R8$$ and $$0\mathcal R1$$.



## Problem 6

For any subset $$A\subseteq\mathbb{R}$$, define $$-A = \{-x: x\in A\}.$$

a) Suppose that $$A$$ is bounded above.  Define the supremum of $$A$$.

b) Suppose that $$A$$ is bounded both above and below.  Prove that $$\sup(-A) = -\inf(A)$$ and $$\inf(-A)=-\sup(A)$$.

**Solution:**

a) It is an upper bound of $$A$$ with the property that any smaller number is not an upper bound.

b) Let $$M=\sup(A)$$.  Then $$M$$ is an upper bound of $$A$$.  Therefore

$$x \leq M\quad \text{for all}\ x\in A.$$

It follows that

$$-M\leq -x \quad \text{for all}\ x\in A,$$

and therefore

$$-M\leq y \quad \text{for all}\ y\in -A.$$

Therefore $$-M$$ is a lower bound of $$-A$$.

If $$a > -M$$, then $$-a < M$$ and therefore $$-a$$ is not an upper bound of $$A$$.
It follows that there exists $$x\in A$$ with $$x > -a$$.
Therefore $$y=-x\in -A$$ satisfies $$y < a$$.
Thus $$a$$ is not a lower bound.
This shows that $$-M$$ is the greatest lower bound, ie. the infimum of $$A$$.
The other half of the problem is proved similarly.

## Problem 7

Consider the set

$$\left\lbrace\frac{2n^2+3}{n^2+2n}: n\in\mathbb{Z}_+\right\rbrace$$

a) Explain why the set has a supremum

b) Find the supremum of the set

c) Carefully prove that the supremum you found is the supremum of the set

**Solution:**

a) First of all

$$\frac{2n^2+3}{n^2+2n} = \frac{2+3/n^2}{1+2/n} \leq \frac{2+3/n^2}{1+2/n} \leq \frac{2+3/n^2}{1} \leq 5.$$

Thereefore the set is bounded above by $$5$$.
By the Completeness Axiom it must have a supremum.

b) The first element of the set is $$5/3$$.  The second is $$11/8$$.  The third is $$21/15$$. Then as $$n$$ gets larger, the elements of the set increase toward $$2$$.  This makes us suspect that the answer might be $$2$$.  Let's prove it.

First of all

$$\frac{2n^2+3}{n^2+2n} = 2 - \frac{4n-3}{n^2+2n} < 2$$

for all $$n\in\mathbb{Z}_+$$.  Therefore $$2$$ is an upper bound for the set.

Moreover, 

$$\frac{4n-3}{n^2+2n} < \frac{4(n-1)}{n(n+2)} < \frac{4}{(n-1)(n+2)} < \frac{4}{n+2}.$$

This means that

$$ \frac{2n^2+3}{n^2+2n} \geq 2 - \frac{4}{n+2}.$$

Now suppose that $$a < 2$$.  Then for $$n$$ an integer greater than $$4/(2-a) - 2$$ we have

$$n+2 > 4/(2-a)$$

and therefore

$$2-a > 4/(n+2)$$

and thus

$$ \frac{2n^2+3}{n^2+2n} \geq 2 - \frac{4}{n+2} > 2 - (2-a) = a.$$

Thus $$a$$ is not an upper bund and this proves $$2$$ is the greatest upper bound.

## Problem 8

Consider the family of sets $$\{A_i: i\in I\}$$
with index set $$I=\mathbb{Z}_+$$ and with 

$$A_i = \{x\in (0,1): \lfloor 10^ix\rfloor \neq 5\mod 10\},$$

where here $$\lfloor y\rfloor$$ denotes the greatest integer less than or equal to $$y$$.
Consider the intersection

$$C=\bigcap_{i\in I} A_i$$

(a) Explain why $$\frac{1}{5}\in C$$

(b) Prove that $$\frac{1}{5}$$ is not an interior point of $$C$$

(c) Prove that $$\frac{1}{5}$$ is an accumulation point of $$C$$ 

**Solution**:

(a) We have that 

$$\lfloor 10^0\frac{1}{5}\rfloor = 0$$

$$\lfloor 10^1\frac{1}{5}\rfloor = 2$$

$$\lfloor 10^j\frac{1}{5}\rfloor = 0\mod 5\quad\text{for all}\ j\geq 2$$

Therefore $$\frac{1}{5}\in A_i$$ for all $$i\in I$$.  Therefore $$\frac{1}{5}\in C$$.

(b) Let $$r>0$$.  The open ball of radius $$r$$ is the open interval

$$B(\frac{1}{5};r) = (1/5-r,1/5+r).$$

Choose $$n\geq 2$$ with $$10^n > 5/r$$ so that $$\frac{5}{10^n} < r$$.
Then

$$x = \frac{1}{5} + 5\cdot 10^{-n} = 0.2000\dots 0500\dots$$

belongs to $$B(\frac{1}{5};r)$$, but $$\lvert 10^nx \rvert = 5\mod 10$$, so $$x\notin A_n$$.
Therefore $$x\notin C$$.
This proves $$B(\frac{1}{5};r)$$ is not contained in $$C$$.
Since $$r>0$$ was arbitrary, this proves that $$\frac{1}{5}$$ isn't an interior point.

(c) Let $$r > 0$$.   

Choose $$n\geq 2$$ with $$10^n > 3/r$$ so that $$\frac{3}{10^n} < r$$.
Then

$$x = \frac{1}{5} + 3\cdot 10^{-n} = 0.2000\dots 0300\dots$$

belongs to $$B(\frac{1}{5};r)$$, and is in $$A_i$$ for all $$i\in I$$.
Therefore $$x\in C$$.
This proves $$B(\frac{1}{5};r)$$ contains a point of $$C$$ different from $$\frac{1}{5}$$>
Since $$r>0$$ was arbitrary, this proves that $$\frac{1}{5}$$ is an accumulation point.





