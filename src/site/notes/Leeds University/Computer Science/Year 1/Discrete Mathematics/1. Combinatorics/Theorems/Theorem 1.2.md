---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/discrete-mathematics/1-combinatorics/theorems/theorem-1-2/","tags":["Theorem"]}
---

For integers ${\color{blue} k}$ and ${\color{red} n}$ such that $0 \leq {\color{blue} k} \leq {\color{red} n}$, the total number of ${\color{blue} k}$-*combinations* of a [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] of ${\color{red} n}$ objects is $C({\color{red} n},{\color{blue} k})=\frac{{\color{red} n}!}{{\color{blue} k}!({\color{red} n}-{\color{blue} k})!}$
{ #Definition}


###### *Proof*
Since a set of ${\color{blue} k}$ elements (${\color{blue} k}$-*permutations*) can be arranged into exactly ${\color{blue} k}!$ sequences,
$P({\color{red} n},{\color{blue} k})=C({\color{red} n},{\color{blue} k}){\color{blue} k}!$
i.e.
In the ${\color{blue} k}$-*combinations* of ${\color{red} n}$, order doesn’t matter
$\therefore$ To ‘make order matter’ you can use the [[Leeds University/Computer Science/Year 1/Discrete Mathematics/1. Combinatorics/1.1 Basic Counting Principles/The Multiplication Principle\|Multiplication Principle]] to order the [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] of ${\color{blue} k}$-*combinations* into the set of ${\color{blue} k}$-*permutations*