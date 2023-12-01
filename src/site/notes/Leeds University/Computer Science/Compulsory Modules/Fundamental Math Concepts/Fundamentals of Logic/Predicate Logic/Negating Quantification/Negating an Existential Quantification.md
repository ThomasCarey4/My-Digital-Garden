---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/predicate-logic/negating-quantification/negating-an-existential-quantification/"}
---


The statement
$$
\color{lightgreen}
\textquoteleft
\text{There is a student in your class who has taken a course in calculus}
\textquoteright
$$
is an [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Quantification/Existential Quantification\|Existential Quantification]], namely
$$
\color{red} 
\exists x\ Q(x)
$$
where $\color{red} Q(x)$ is the statement $\color{red} \textquoteleft x\text{ has taken a course in calculus} \textquoteright$ and the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|domain]] consists of all the students in you class
What is the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Negation\|negation]]?
$$
\begin{align}
\color{lightgreen}
\textquoteleft
&\color{lightgreen} \text{It is not the case that} \\
&\color{lightgreen} \text{there exists a student in your class who has taken a course in calculus}
\textquoteright
\end{align}
$$
How can this also be expressed?
$$
\color{lightgreen}
\textquoteleft
\text{Every student in you class has not taken a course in calculus}
\textquoteright
$$
Therefore...
$$
\color{red} 
\neg{\exists x\ Q(x)} \equiv \forall x\ \neg{Q(x)}
$$