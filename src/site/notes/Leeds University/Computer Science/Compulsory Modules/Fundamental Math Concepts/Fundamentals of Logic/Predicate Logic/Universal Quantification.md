---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/predicate-logic/universal-quantification/"}
---


$$
\color{red}'P(x)\ for\ all\ values\ of\ x\ in\ the\ domain\ of\ x'
$$
- The notation $\color{red}\forall x\ P(x)$ denotes the universal quantification of $P(x)$
- The symbol $\color{red}\forall$ is called the universal quantifier
- We read $\forall x\ P(x)$ as $\color{red}'for\ all\ x\ P(x)'$ or $\color{red}'for\ every\ x\ P(x)'$
- The domain of x is a $\color{lightgreen}set$. We have to specify the domain of x
An element of which $P(x)$ is false is called a **[[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Sets#Counterexamples\|counterexample]]** to $\forall x\ P(x)$

>Note that if the domain is empty, then $\forall x\ P(x)$ is true for every propositional function $P(x)$ because there are no elements $x$ in the domain for which $P(x)$ is false.

### Counterexamples
When is a statement $\color{red}\forall x\ P(x)$ false?

A statement $\forall x\ P(x)$ is false on a given domain, [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Biconditional\|if and only if]] there is at least one element in $x$ in the domain for which $P(x)$ is false

One way to show that $\forall x\ P(x)$ is not true on the given domain is to find a **counterexample** to the statement $\forall x\ P(x)$

A single counterexample is all we need to establish that $\forall x\ P(x)$ is false

### Finite Domains
When the domain is $\color{red} finite$, i.e. when all the elements in the domain can be listed, say, $x_1,x_2,...,x_n$ it follows that the universal quantification $\color{red}\forall x\ P(x)$ expresses the same as the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Conjunction\|conjunction]]
$$
\color{red}P(x_{1})\land P(x_{2})\land\ ...\ \land P(x_{n})
$$
because this [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Conjunction\|conjunction]] is true [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Biconditional\|if and only if]] all $\color{red}P(x_{1})\color{white},\color{red}P(x_{2})\color{white},\ ...\ ,\color{red}P(x_{n})$
are true
#TODO you got more to do silly little man