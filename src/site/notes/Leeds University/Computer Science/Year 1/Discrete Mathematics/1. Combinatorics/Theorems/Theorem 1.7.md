---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/discrete-mathematics/1-combinatorics/theorems/theorem-1-7/","tags":["Theorem"]}
---

Let ${\color{lightgreen} m},{\color{red} n}$ and ${\color{lavender} r}$ be non-negative integers with ${\color{orange} r} \leq {\color{lightgreen} m}, {\color{red} n}$. Then
$\tbinom{{\color{lightgreen} m}+{\color{red} n}}{{\color{lavender} r}}=\sum\limits^{\color{lavender} r}_{{\color{blue} k}=0}\tbinom{{\color{lightgreen} m}}{{\color{lavender} r}-{\color{blue} k}}\tbinom{{\color{red} n}}{{\color{blue} k}}$
{ #Definition}


###### *Proof*:
Suppose there are ${\color{lightgreen} m}$ items in one [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] and ${\color{red} n}$ (different) items in a second [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]]
Then the total number of ways to pick ${\color{lavender} r}$ related elements from the [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.19 (Set Operations)\|union]] of these [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|sets]] is $\tbinom{{\color{lightgreen} m}+{\color{red} n}}{{\color{lavender} r}}$
Another way to pick ${\color{lavender} r}$ elements from the [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.19 (Set Operations)\|union]] is to pick ${\color{blue} k}$ elements from the first [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] and then ${\color{lavender} r}-{\color{blue} k}$ elements from the second [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]], where ${\color{blue} k}$ is an integer with $0\leq {\color{blue} k}\leq {\color{lavender} r}$
This can be done in $\tbinom{{\color{lightgreen} m}}{{\color{blue} k}}\tbinom{{\color{red} n}}{{\color{lavender} r}-{\color{blue} k}}$ ways, using the [[Leeds University/Computer Science/Year 1/Discrete Mathematics/1. Combinatorics/1.1 Basic Counting Principles/The Multiplication Principle\|product rule]], and so the total is $\sum\limits^{\color{lavender} r}_{{\color{blue} k}=0}\tbinom{{\color{lightgreen} m}}{{\color{blue} k}}\tbinom{{\color{red} n}}{{\color{lavender} r}-{\color{blue} k}}$
Therefore, $\tbinom{{\color{lightgreen} m}+{\color{red} n}}{{\color{lavender} r}}=\sum\limits^{\color{lavender} r}_{{\color{blue} k}=0}\tbinom{{\color{lightgreen} m}}{{\color{lavender} r}-{\color{blue} k}}\tbinom{{\color{red} n}}{{\color{blue} k}}$
