---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/proof-techniques/proof-by-induction/"}
---

By $\color{red} \mathbb{N}$ we denote the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] of all $\color{red}\text{natural numbers}$ (i.e. $\mathbb{N} \coloneqq \set{0,1,2,3,...}$)

Let $P(n)$ be a statement about a natural number $n$
- This is called the $\color{red}\text{induction hypothesis}$
The aim is to prove that statement $P(n)$ is true **for every** $n \in \mathbb{N}$. One method to do this is by $\color{red}\text{mathematical induction}$:

1. First, we prove that statement $P(n)$ is true for $n=0$.
    We call this step $\color{red}\text{basis of the induction}$, or simply $\color{red}\text{basis step}$
2. In the second step, we prove for every natural number $n \in \mathbb{N}$:
    **If** statement $P(n)$ is true, **then** the statement $P(n+1)$ is true as well.
    This step is called the $\color{red}\text{inductive step}$

Altogether, this proves that statement $P(n)$ is true $\color{red}\text{for all}$ $n \in \mathbb{N}$
##### Strong Induction
Equivalent to 'normal' induction, however you can assume that every number in the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] less than $n$ ( $n_{0} \leq i \leq n$ ) is also true when proving $P(n+1)$
