---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/predicate-logic/quantification/existential-quantification/"}
---

The $\color{red}\text{existential quantification}$ of $P(x)$ is the statement
$$
\color{red}
\textquoteleft\text{There exists an element }x\text{ in the domain such that }P(x)\textquoteright
$$
- The notation $\color{red}\exists x\ P(x)$ denotes the existential quantification of $P(x)$
- The symbol $\color{red}\exists$ is called the $\color{red} \text{existential quantifier}$
- We read $\exists x\ P(x)$ as $\color{red} \textquoteleft \text{there exists an }x\ P(x)\textquoteright$ or $\color{red} \textquoteleft \text{there is an }x\ P(x) \textquoteright$

The existential quantification $\exists x\ P(x)$ can be expressed as
- 'There is an $x$ such that $P(x)$'
- 'There is at least one $x$ such that $P(x)$'
- 'For some $x$ $P(x)$'

#### Remarks
- A [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|domain]] must always be specified when a statement $\exists x\ P(x)$ is used
- The meaning of $\exists x\ P(x)$ changes when the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|domain]] changes
- Without specifying the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|domain]], the statement $\exists x\ P(x)$ has no meaning

### Finite [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|Domains]]
When the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|domain]] is $\color{red} finite$, i.e. when all the elements in the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|domain]] can be listed, say, $x_1,x_2,...,x_n$ it follows that the existential quantification $\color{red}\exists x\ P(x)$ expresses the same as the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Disjunction\|disjunction]]
$$
\color{red}P(x_{1})\lor P(x_{2})\lor\ ...\ \lor P(x_{n})
$$
because this [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Disjunction\|disjunction]] is true [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Biconditional\|if and only if]] at least one $\color{red}P(x_{1})\color{white},\color{red}P(x_{2})\color{white},\ ...\ ,\color{red}P(x_{n})$ is true
- If the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|domain]] is empty, the existential quantifier is false
