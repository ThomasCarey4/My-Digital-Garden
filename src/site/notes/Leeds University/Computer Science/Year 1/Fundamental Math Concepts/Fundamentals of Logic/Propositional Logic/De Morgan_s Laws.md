---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/fundamental-math-concepts/fundamentals-of-logic/propositional-logic/de-morgan-s-laws/"}
---

De Morgan's Laws tell us how to negate [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Conjunction\|Conjunctions]] and [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Disjunction\|Disjunctions]]

For example, ***'Miguel has a mobile phone and he has a laptop'***
$$
\begin{flalign}
p &\coloneqq Miguel\ has\ a\ mobile\ phone &&\\
q &\coloneqq Miguel\ has\ a\ laptop &&\\
\end{flalign}
$$$$
\begin{align}
S &= p \land q \\
\therefore \neg{S} &= \neg{(p \land q)} \\
&\equiv \neg{p} \lor \neg{q}
\end{align}
$$
Therefore, through the use of De Morgan's Laws, we known the negation of the original statement is:
***'Miguel does not have a mobile or he does not have a laptop'***
