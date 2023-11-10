---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/proof-techniques/proof-by-induction/"}
---

By $\color{red} \mathbb{N}$ we denote the set of all $\color{red}\text{natural numbers}$ (i.e. $\mathbb{N} \coloneqq \set{0,1,2,3,...}$)

Let $P(n)$ be a statement about a natural number $n$ The aim is to prove that statement $P(n)$ is true **for every** $n \in \mathbb{N}$. One method to do this is by $\color{red}\text{mathematical induction}$:

1. First, we prove that statement $P(n)$ is true for $n=0$.
    We call this step $\color{red}\text{basis of the induction}$, or simply $\color{red}\text{basis step}$
2. In the second step, we prove for every natural number $n \in \mathbb{N}$:
    **If** statement $P(n)$ is true, **then** the statement $P(n+1)$ is true as well.
    This step is called the $\color{red}\text{inductive step}$

Altogether, this proves that statement $P(n)$ is true $\color{red}\text{for all}$ $n \in \mathbb{N}$
