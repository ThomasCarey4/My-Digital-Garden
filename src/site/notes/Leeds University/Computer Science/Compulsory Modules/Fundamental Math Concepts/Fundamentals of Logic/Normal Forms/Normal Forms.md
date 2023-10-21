---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/normal-forms/normal-forms/"}
---

***Normal Forms are used to find the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] from Boolean Algebra from the result***
##### The two types of Normal Forms:

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/normal-forms/disjunctive-normal-form/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




A [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|propositional]] [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] is in <span style="color:#ff0000">Disjunctive Normal Form (DNF)</span>, if it is a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Disjunction\|Disjunction]] of [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Conjunction\|Conjunctions]] of [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Literal\|literals]], i.e. if it is of the form
$
\bigvee^{n}_{i=1}(\bigwedge^{m_i}_{j=1}\ell_{i,j})
$
Where $n, m_1,...,m_{n}\in\mathbb{N}_{>0}$ and $\ell_{i,j}$ is a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Literal\|literal]]
( for every $i\in\{1,...,n\},j\in\{1,...,m_{i}\}$ )

The sub-[[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formulas]] $\bigwedge^{m_i}_{j=1}\ell_{i,j}$ ( for $i\in\{1,...,n\}$ ) are called <span style="color:#ff0000">Conjunctive Clauses</span>.

</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/normal-forms/conjunctive-normal-form/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




A [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|propositional]] [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] is in <span style="color:#ff0000">Conjunctive Normal Form (DNF)</span>, if it is a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Conjunction\|Conjunction]] of [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Disjunction\|Disjunctions]] of [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Literal\|literals]], i.e. if it is of the form
$
\bigwedge^{n}_{i=1}(\bigvee^{m_i}_{j=1}\ell_{i,j})
$
Where $n, m_1,...,m_{n}\in\mathbb{N}_{>0}$ and $\ell_{i,j}$ is a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Literal\|literal]]
( for every $i\in\{1,...,n\},j\in\{1,...,m_{i}\}$ )

The sub-[[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formulas]] $\bigvee^{m_i}_{j=1}\ell_{i,j}$ ( for $i\in\{1,...,n\}$ ) are called <span style="color:#ff0000">Disjunctive Clauses</span>.

</div></div>



We let $\mathbb{N}$ denote the set of all natural numbers including 0
We let $\mathbb{N}_{>0}$ denote the set of all natural numbers excluding 0

We use **'[[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]]'** to mean *'proposition or compound proposition'*

For an $n \in \mathbb{N}_{>0}\ {}$, let $p1,p2,p3,...,p_n$ be $n$ [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formulas]]. Then we define:
$$
\begin{align*}
&\color{red} \bigwedge^{n}_{i=1} p_{i} \color{white}
\coloneqq p_{1} \land p_{2} \land p_{3}\ \land \ ...\ \land\ p_{n}, \\
&\color{red} \bigvee^{n}_{i=1} p_{i} \color{white}
\coloneqq p_{1} \lor p_{2} \lor p_{3}\ \lor \ ...\ \lor\ p_{n}. \\
\end{align*}
$$

For every [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|propositional]] [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] $p$ there is a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] $p_D$ in [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Normal Forms/Disjunctive Normal Form\|DNF]] and a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] $p_C$ in [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Normal Forms/Conjunctive Normal Form\|CNF]], such that $p\equiv p_{D}$ and $p\equiv p_{C}$ 

In other words: <span style="color:#ff0000">Every formula is equivalent to a formula in DNF and to a formula in CNF</span>
