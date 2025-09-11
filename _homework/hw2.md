---
layout: page
title: Homework 1
permalink: /homework/hw1
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

**Problem 1:** Let $$f: S\rightarrow T$$ be a function.  The **inverse image** or **preimage**  of a set $$B\subseteq T$$ is the set

$$f^{-1}(B) = \{x\in S: f(x)\in B\}$$

and the **image** of a set $$A\subseteq S$$ is

$$f(A) = \{f(x): x\in A\}$$

Prove the following for $$A\subseteq S$$ and $$B\subseteq T$$

* (a) $$A\subseteq f^{-1}(f(A))$$ 
* (b) $$f(f^{-1}(B))\subseteq B$$
* (c) $$f^{-1}(T-B)=S-f^{-1}(B)$$

**Problem 2:** Let $$f: S\rightarrow T$$ be a function and suppose that $$\{A_i: i\in I\}$$ is a family of subsets of $$S$$ and $$\{B_j: j\in J\}$$ is a family of subsets of $$T$$.  Prove that

* (a) $$f^{-1}\left(\bigcup_{j\in J}B_j\right) = \bigcup_{j\in J}f^{-1}(B_j)$$
* (b) $$f^{-1}\left(\bigcap_{j\in J}B_j\right) = \bigcap_{j\in J}f^{-1}(B_j)$$
* (c) $$f\left(\bigcup_{i\in I}A_i\right) = \bigcup_{i\in I}f(A_i)$$
* (d) $$f\left(\bigcap_{i\in I}A_i\right) \subseteq \bigcap_{i\in I}f(A_i)$$
* (e) Show by example that the intersections in (d) may not be equal

**Problem 3:** Let $$f: S\rightarrow T$$ be a function.  Prove that the following statements are equivalent.
* (i) $$f$$ is one-to-one
* (ii) $$f(A\cap C) = f(A)\cap f(C)$$ for all subsets $$A,C\subseteq S$$
* (iii) $$f^{-1}(f(A)) = A$$ for all $$A\subseteq S$$
* (iv) for all *disjoint* subsets $$A,C\subseteq S$$, the images $$f(A)$$ and $$f(C)$$ are disjoint
* (v) for all subsets $$A,C\subseteq S$$ with $$C\subseteq A$$ we have $$f(A-C)=f(A)-f(C)$$

**Problem 4:** Prove that if $$S$$ is an infinite set, then $$S$$ contains a countably infinite subset.

**Problem 5:** Prove that if $$S$$ is an infinite set and $$a\in S$$, then $$S$$ and $$S-\{a\}$$ have the same cardinality.

**Problem 6:** A **binary function** on a set $$S$$ is a function whose values are either $$0$$ or $$1$$.  Prove that the set of all binary functions on $$\mathbb Z_+$$ is uncountable.


