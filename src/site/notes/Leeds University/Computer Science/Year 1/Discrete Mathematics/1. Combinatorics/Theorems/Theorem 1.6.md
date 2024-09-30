---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/discrete-mathematics/1-combinatorics/theorems/theorem-1-6/","tags":["Theorem"]}
---

Let ${\color{red} n}$ and ${\color{blue} k}$ be positive integers with ${\color{red} n} \geq {\color{blue} k}$. Then $\binom{{\color{red} n}+1}{{\color{blue} k}}=\binom{{\color{red} n}}{{\color{blue} k}-1}+\binom{{\color{red} n}}{{\color{blue} k}}$
{ #Definition}


###### *Proof*:
Let ${\color{orange} T}$ be a [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] containing ${\color{red} n}+1$ elements. Let ${\color{lightgreen} a}\in {\color{orange} T}$ and ${\color{lavender} S}={\color{orange} T}\ \backslash \set{a}$
There are $\tbinom{{\color{red} n}+1}{{\color{blue} k}}$ [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.5 (Subsets and Supersets)\|subsets]] of ${\color{orange} T}$ containing ${\color{blue} k}$ elements.

A [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.5 (Subsets and Supersets)\|subset]] of ${\color{orange} T}$ with ${\color{blue} k}$ elements either contains ${\color{lightgreen} a}$ together with ${\color{blue} k}-1$ elements of ${\color{lavender} S}$, or contains ${\color{blue} k}$ elements of ${\color{lavender} S}$ and does **not** contain ${\color{lightgreen} a}$.

So there are $\tbinom{{\color{red} n}}{{\color{blue} k}-1}$ [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.5 (Subsets and Supersets)\|subsets]] of ${\color{orange} T}$ with ${\color{blue} k}$ elements that contain ${\color{lightgreen} a}$, and $\tbinom{{\color{red} n}}{{\color{blue} k}}$ [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.5 (Subsets and Supersets)\|subsets]] of ${\color{orange} T}$ with ${\color{blue} k}$ elements that do not contain ${\color{lightgreen} a}$
Therefore, $\tbinom{{\color{red} n}+1}{{\color{blue} k}}=\tbinom{{\color{red} n}}{{\color{blue} k}-1}+\tbinom{{\color{red} n}}{{\color{blue} k}}$
