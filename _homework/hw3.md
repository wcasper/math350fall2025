---
layout: page
title: Homework 3
permalink: /homework/hw3
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

Decide, with proof, whether each of the following subsets of $$\mathbb R^2$$ are open, closed or neither.

a) all points $$(x,y)$$ such that $$x^2 - y^2  < 1$$  

Hint: let 

$$U = \{(x,y)\in\mathbb R^2: x^2-y^2 < 1\}$$

and suppose $$(a,b)\in U$$.  If $$b=0$$ take $$r=1-\lvert a\rvert$$.  Otherwise, take the radius to be 

$$r=\min\left(\frac{1+b^2-a^2}{2(\lvert a\rvert + \lvert b\rvert)},\frac{1}{2}\lvert b\rvert\right).$$

and let $$(x,y)$$ be in the ball of radius $$r$$ around $$(a,b)$$.  In the latter case,

$$x^2 < (\lvert a\rvert + r)^2\ \ \text{and}\ \ y^2 > (\lvert b\rvert - r)^2.$$

Use this to prove that the ball is contained in $$U$$.


b) all points $$(x,y)$$ such that $$x > 0$$

c) all points $$(x,y)$$ such that $$x \geq 0$$


**Problem 2:** 

Suppose that $$A,B\subseteq\mathbb R^n$$.  Prove the following:

a) $$\text{int}(A)\cap\text{int}(B) = \text{int}(A\cap B)$$

b) $$\text{int}(A)\cup\text{int}(B) \subseteq \text{int}(A\cup B)$$

c) Show by example that there exists $$A$$ and $$B$$ with $$\text{int}(A)\cup\text{int}(B) \neq \text{int}(A\cup B)$$

**Problem 3:** 

Suppose that $$A,B\subseteq\mathbb R^n$$.  Prove the following:

a) $$\overline{A\cap B} \subseteq \overline{A}\cap \overline{B}$$

b) if $$A$$ is open, then $$A\cap\overline{B} \subseteq \overline{A\cap B}$$

**Problem 4:** 

a) Give an example of a set $$A\subseteq \mathbb R^n$$ which is closed but not bounded.  Carefully explain why it is closed and why it is not bounded.

b) For the set $$A$$ you chose, given an example of a countable open cover of $$A$$ without a finite subcover.  Carefully explain why there is no finite subcover.

**Problem 5:** 

Consider the family of open sets $$\{U_i: i\in I\}$$ in $$\mathbb R^2$$, with index set $$I = \mathbb Q$$ and

$$U_r = B((r,r),r) = \{(x,y)\in\mathbb R^2: \sqrt{(x-r)^2+(y-r)^2} < r\}.$$

Prove that this defines an open covering of the first quadrant

$$A = \{(x,y)\in\mathbb R^2: x > 0,\ y > 0\}.$$



