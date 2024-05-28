---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/discrete-mathematics/1-combinatorics/1-1-basic-counting-principles/the-multiplication-principle/"}
---

###### The Multiplication Principle for Counting Procedures
If a sequence can be described as a sequence of ${\color{red} n}$ *independent* steps, with ${\color{blue} i}_{1}$ possible outcomes for the first step, ${\color{blue} i}_{2}$ possible outcomes for the second step, $\dots$, and ${\color{blue} i}_{{\color{red} n}}$ possible outcomes for the ${\color{red} n}^{th}$ step, then the total number of composite outcomes of the procedure is ${\color{blue} i}_{1}{\color{blue} i}_{2}\dots{\color{blue} i}_{{\color{red} n}}$
###### <hr>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/discrete-mathematics/1-combinatorics/1-1-basic-counting-principles/sequential-counting-procedures/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




A *sequential counting procedure* is one that satisfies the following three properties:
1. The steps are ***ordered***, i.e. any two sequences of different outcomes represent distinguishable composite outcomes
2. The steps are ***independent***, i.e. the number of outcomes of one step is not affected by the outcomes of the preceding steps
3. The steps are ***complete***, i.e. each composite outcome consists of a complete sequence of individual outcomes, one for each step


</div></div>


>[!example] 
>A binary sequence is a sequence whose elements come from the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] $\set{0,1}$. For example, 100110 is a binary sequence of length 6
>1. How many binary sequences of length 5 are there?
>2. How many binary sequences of length 5 begin with 101?

**Part 1:**
Each step ${\color{blue} i}$ has 2 possible outcomes $\set{0,1}$
${\color{red} n} = 5$
$\therefore$ The total number of composite outcomes, $\prod_{r=1}^{{\color{red} n}} \limits {{\color{blue} i}_{r}}$, is $2^{{\color{red} 5}}$
**Part 2:**
${\color{blue} i}_{1},{\color{blue} i}_{2},{\color{blue} i}_{3}$ all have one option, making 101
The steps ${\color{blue} i}_{4},{\color{blue} i}_{5}$ choose from $\set{0,1}$
${\color{red} n}=5$
$\therefore$ $\prod_{r=1}^{{\color{red} n}} \limits {{\color{blue} i}_{r}}=\prod_{r=4}^{{\color{red} 5}} \limits {{\color{blue} i}_{r}}=2^{2}$
