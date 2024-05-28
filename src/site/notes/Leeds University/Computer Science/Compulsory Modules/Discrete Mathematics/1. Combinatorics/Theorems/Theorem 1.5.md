---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/discrete-mathematics/1-combinatorics/theorems/theorem-1-5/","tags":["Theorem"]}
---

If ${\color{lavender} a}$ and ${\color{orange} b}$ are real numbers and ${\color{red} n}$ is a positive integer, then $({\color{lavender} a}+{\color{orange} b})^{\color{red} n}=\sum\limits^{\color{red} n}_{{\color{blue} k}=0}\binom{{\color{red} n}}{{\color{blue} k}}{\color{lavender} a}^{{\color{red} n}-{\color{blue} k}}{\color{orange} b}^{\color{blue} k}$
{ #Definition}


###### *Proof*: $\color{white} ({\color{lavender} a}+{\color{orange} b})^{\color{red} n}=({\color{lavender} a}+{\color{orange} b})\dots({\color{lavender} a}+{\color{orange} b})\ ({\color{red} n}\text{ factors})$
In the expansion of $({\color{lavender} a}+{\color{orange} b})^{\color{red} n}$, a term of the form ${\color{lavender} a}^{{\color{red} n}-{\color{blue} k}}{\color{orange} b}^{\color{blue} k}$ arises from choosing ${\color{orange} b}$ from ${\color{blue} k}$ factors and ${\color{lavender} a}$ from the other ${\color{red} n}-{\color{blue} k}$ factors. This can be done in $\binom{{\color{red} n}}{{\color{blue} k}}$ ways. Thus ${\color{lavender} a}^{{\color{red} n}-{\color{blue} k}}{\color{orange} b}^{\color{blue} k}$ appears $\binom{{\color{red} n}}{{\color{blue} k}}$ times in the expansion. It follows that:
$$
\begin{align}
&({\color{lavender} a}+{\color{orange} b})^{\color{red} n} \\
&={\tiny\binom{{\color{red} n}}{0}}{\color{lavender} a}^{{\color{red} n}-1}{\color{orange} b}^{1}+{\tiny\binom{{\color{red} n}}{2}}{\color{lavender} a}^{{\color{red} n}-2}{\color{orange} b}^{2}+\dots+{\tiny\binom{{\color{red} n}}{{\color{red} n}-1}}{\color{lavender} a}^{1}{\color{orange} b}^{{\color{red} n}-1}+{\tiny\binom{{\color{red} n}}{{\color{red} n}}}{\color{lavender} a}^{0}{\color{orange} b}^{\color{red} n} \\
&=\small\sum\limits^{\color{red} n}_{{\color{blue} k}=0}{\tiny\binom{{\color{red} n}}{{\color{blue} k}}}{\color{lavender} a}^{{\color{red} n}-{\color{blue} k}}{\color{orange} b}^{\color{blue} k}
\end{align}
$$
The numbers $\binom{{\color{red} n}}{{\color{blue} k}}$ are known as *binomial coefficients* because they appear in the expansion of $({\color{lavender} a}+{\color{orange} b})^{\color{red} n}$
