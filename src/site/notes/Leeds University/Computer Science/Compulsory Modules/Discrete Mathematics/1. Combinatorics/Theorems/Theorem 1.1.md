---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/discrete-mathematics/1-combinatorics/theorems/theorem-1-1/","tags":["Theorem"]}
---

For integers ${\color{blue} k}$ and ${\color{red} n}$ such that $0\leq {\color{blue} k} \leq {\color{red} n}$, the number of ${\color{blue} k}$-*permutations* of a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] of ${\color{red} n}$ objects is $P({\color{red} n}, {\color{blue} k})=\frac{{\color{red} n}!}{({\color{red} n}-{\color{blue} k})!}$^Definition
###### *Proof*
First suppose that ${\color{blue} k}=0$.
Then $P({\color{red} n},0)$ and $\frac{{\color{red} n}!}{({\color{red} n}-0)!}=\frac{{\color{red} n}!}{{\color{red} n}!}=1$, and hence the result holds
Now assume that $1\leq {\color{blue} k}$, and consider the following counting procedure:
1. Choose an element for the first position (${\color{red} n}$ choices)
2. Choose an element for the second position (${\color{red} n}-1$ choices)
$\dots$
3. Choose an element for the ${\color{blue} k}^{th}$ position (${\color{red} n}-{\color{blue} k}+1$ choices)
So, by the [[Leeds University/Computer Science/Compulsory Modules/Discrete Mathematics/1. Combinatorics/1.1 Basic Counting Principles/The Multiplication Principle\|Multiplication Principle]], $P({\color{red} n}, {\color{blue} k})={\color{red} n}({\color{red} n}-1)\dots({\color{red} n}-{\color{blue} k}+1)$
$\frac{{\color{red} n}!}{({\color{red} n}-{\color{blue} k})!}=\frac{{\color{red} n}({\color{red} n}-1)\dots({\color{red} n}-{\color{blue} k}+1)({\color{red} n}-{\color{blue} k})!}{({\color{red} n}-{\color{blue} k})!}={\color{red} n}({\color{red} n}-1)\dots({\color{red} n}-{\color{blue} k}+1)$, and hence the result holds true

*Note that $P({\color{red} n},{\color{red} n})={\color{red} n}!$*
