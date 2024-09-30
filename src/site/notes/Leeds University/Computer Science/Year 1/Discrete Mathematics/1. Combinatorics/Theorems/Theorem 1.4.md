---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/discrete-mathematics/1-combinatorics/theorems/theorem-1-4/","tags":["Theorem"]}
---

For positive integer ${\color{blue} k}$ and ${\color{red} n}$, the number of ${\color{blue} k}$-*combinations* with *unlimited repetition* of a set of ${\color{red} n}$ objects is $C({\color{blue} k}+{\color{red} n}-1,{\color{blue} k})=\frac{({\color{blue} k}+{\color{red} n}-1)!}{{\color{blue} k}!({\color{red} n}-1)!}$
{ #Definition}


###### *Proof*
>[!example] 
>In how many ways can 7 identical balls be distributed into 3 distinct boxes?

${\color{blue} k}=7$
${\color{red} n}=3$
If we model this problem as a set of $7\ ({\color{blue} k})$ 0’s (for the balls) and $2\ ({\color{red} n}-1)$ |’s for the ‘walls’
i.e. 000 | 00 | 00 $\implies$ an example distribution of 3 boxes

To solve this we can do $C(9,7)$, choose 7 positions from 9
i.e. 0 0 0 \_ 0 0 \_ 0 0
Now, we place the |’s in the only available positions (1 way)
$\therefore$ The answer is $C(9,7)=\frac{9!}{7!2!}$
$C(9,7)=C(9,2)$
$=C({\color{blue} k}+{\color{red} n}-1,{\color{blue} k})$
$=C({\color{blue} k}+{\color{red} n}-1,{\color{red} n}-1)$
By [[Leeds University/Computer Science/Year 1/Discrete Mathematics/1. Combinatorics/Theorems/Theorem 1.2\|Theorem 1.2]], $C({\color{blue} k}+{\color{red} n}-1,{\color{blue} k})=\frac{({\color{blue} k}+{\color{red} n}-1)!}{{\color{blue} k}!({\color{red} n}-1)!}$
