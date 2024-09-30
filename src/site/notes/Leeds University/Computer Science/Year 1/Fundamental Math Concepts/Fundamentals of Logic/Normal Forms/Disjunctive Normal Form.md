---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/fundamental-math-concepts/fundamentals-of-logic/normal-forms/disjunctive-normal-form/"}
---

A [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|propositional]] [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|Formula]] is in <span style="color:#ff0000">Disjunctive Normal Form (DNF)</span>, if it is a [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Disjunction\|Disjunction]] of [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Conjunction\|Conjunctions]] of [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Literal\|literals]], i.e. if it is of the form
$$
\bigvee^{n}_{i=1}(\bigwedge^{m_i}_{j=1}\ell_{i,j})
$$
Where $n, m_1,...,m_{n}\in\mathbb{N}_{>0}$ and $\ell_{i,j}$ is a [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Literal\|Literal]]
( for every $i\in\{1,...,n\},j\in\{1,...,m_{i}\}$ )

The sub-[[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formulas]] $\bigwedge^{m_i}_{j=1}\ell_{i,j}$ ( for $i\in\{1,...,n\}$ ) are called <span style="color:#ff0000">Conjunctive Clauses</span>.