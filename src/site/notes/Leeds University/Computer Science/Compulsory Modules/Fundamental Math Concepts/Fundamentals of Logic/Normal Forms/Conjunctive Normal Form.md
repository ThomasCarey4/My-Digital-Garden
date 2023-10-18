---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/normal-forms/conjunctive-normal-form/"}
---

A propositional [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] is in <span style="color:#ff0000">Conjunctive Normal Form (DNF)</span>, if it is a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Conjunction\|Conjunction]] of [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Disjunction\|Disjunctions]] of [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Literal\|literals]], i.e. if it is of the form
$$
\bigwedge^{n}_{i=1}(\bigvee^{m_i}_{j=1}\ell_{i,j})
$$
Where $n, m_1,...,m_{n}\in\mathbb{N}_{>0}$ and $\ell_{i,j}$ is a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Literal\|literal]]
( for every $i\in\{1,...,n\},j\in\{1,...,m_{i}\}$ )

The sub-[[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formulas]] $\bigvee^{m_i}_{j=1}\ell_{i,j}$ ( for $i\in\{1,...,n\}$ ) are called <span style="color:#ff0000">Disjunctive Clauses</span>.