---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/set-theory/sets/"}
---


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/definitions/definition-5-1-sets/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




A $\color{red}\text{set}$ is an unordered collection of objects, called $\color{red}\text{elements}$ or $\color{red}\text{members}$ of the set. A set is said to $\color{red}\text{contain}$ its elements.

</div></div>


#### Notation
$\color{red} x \in A$ denotes that **x is an element** of the set A.
$\color{red} x \notin A$ denotes that **x is not an element** of the set A.
$$
\begin{align}
\mathbb{N}&\coloneqq\set{0,1,2,3,\cdots} \text{ The Set of Natural Numbers} \\
\mathbb{Z}&\coloneqq\set{0,1,-1,2,-2,3,-3,\cdots} \text{ The Set of Integers} \\
\mathbb{N}^{+}&\coloneqq\set{1,2,3,\cdots} \text{ The Set of Positive Natural Numbers} \\
\mathbb{Q}&\coloneqq\set{\frac{a}{b} | a,b \in \mathbb{Z}, b \neq 0} \text{ The set of Rational Numbers} \\
\mathbb{R}&\coloneqq \text{ The set of Real Numbers} \\
\mathbb{R}^{+}&\coloneqq \text{ The set of Positive Real Numbers} \\
\end{align}
$$
#### Defining Sets
##### By Enumeration
$$
\color{lightgreen}A\coloneqq\set{0,1,2,3,4,5}=\set{0,1,2,\cdots,5}
$$
This is called the **roster method** ( or **extensional** set notation )
##### By characteristic properties
$$
\begin{align}
\color{lightgreen}B\coloneqq\set{x\ |\ x\in A\ and\ x\ is\ even}
\end{align}
$$
This is called the **set builder notation** ( or **intentional** set notation )

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/definitions/definition-5-3-empty-set/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




The $\color{red}\text{empty set}$ is the ( uniquely determined ) set that contains no element(s)
We denote it by $\color{red} \emptyset$, or by $\color{red} \set{}$


</div></div>

A set with exactly one element is also called a $\color{red}\text{singleton set}$
### Fundamentals
- $\color{red}\text{All elements in a set are distinct.}$
- $\color{red}\text{The elements of a set do not come with a fixed ordering.}$
- $\color{red}\text{The same set can be described in different ways.}$


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/definitions/definition-5-5-subsets-and-supersets/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




Let A, B be [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Set Theory/Sets\|sets]]
1. A is a $\color{red}\text{subset}$ of B (short: $\color{red} A\subseteq B$), if every element of A is also an element of B
2. A is a $\color{red}\text{proper subset}$ of B (short: $\color{red} A \subsetneq B$), if $A\subseteq B$ and $A \neq B$
3. A is a $\color{red}\text{superset}$ of B (short: $\color{red} A\supseteq B$), if $B\subseteq A$
4. A is a $\color{red}\text{proper superset}$ of B (short: $\color{red} A\supsetneq B$), if $A\supseteq B$ and $A \neq B$
###### Remark
Alternative notation for $\color{red} \subsetneq\textcolor{white}{:}$ $\color{red} \subset$


</div></div>

