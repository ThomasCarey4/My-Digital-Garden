---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/predicate-logic/predicate-logic/"}
---

Predicates are statements involving variables, such as
$$
\begin{align}
\color{lightgreen}
x\ &\color{lightgreen}>3, \\
\color{lightgreen}
x\ &\color{lightgreen}=y+3, \\
\color{lightgreen}
z\ &\color{lightgreen}=x+y
\end{align}
$$
$$
\text{and}
$$
$$
\color{lightgreen}\text{Computer }x\text{ is under attack by an intruder}
$$
$$
\text{and}
$$
$$
\color{lightgreen}\text{Computer }x\text{ is functioning properly}
$$
are often found in mathematical assertions, in computer programs, and in system specifications.

These statements are called [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Free and Bound Variables\|free variables]] as they are neither true nor false when the values of the variables are not specified
### Predicate and [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|Propositional]] Functions
The statement $\textquoteleft\color{red}x\color{lightgreen}\text{ is greater than 3}\color{white}\textquoteright$ has two parts
$\color{red}\boxed{O}$ = The variable $\color{red}x$, is the ***subject*** of the statement
$\color{lightgreen}\boxed{O}$ = The ***predicate*** $\color{lightgreen}\textquoteleft\text{is greater than 3}\textquoteright$, refers to *a property that the subject of the statement **may or may not have***

We can denote the statement $\textquoteleft\color{red}x\color{lightgreen}\text{ is greater than 3}\color{white}\textquoteright$ by $\color{red}P(x)$, where *P* denotes the predicate 'is greater than 3' and $x$ is the variable

The statement *$P(x)$* is also said to be the value of the $\color{red}\text{propositional function}$ $P$ and $x$

Once the variable $x$ is [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Free and Bound Variables\|bound]] ( is assigned a value) the statement $P(x)$ becomes a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|proposition]] ( also called a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Free and Bound Variables#^Sentence\|sentence]] ) and has a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Truth Value\|truth value]]

#### More Than One Variable?
We can also have statements that involve more than one variable. For instance, consider the statement $\color{red}x=y+3$

We can denote this statement by $\color{red}Q(x,y)$, where $x$ and $y$ are variables and $\color{red}Q$ is the predicate

Once values are assigned to the variables $x$ and $y$, the statement $\color{red}Q(x,y)$ becomes a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|proposition]] and has a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Truth Value\|truth value]]

### *n*-ary Predicates
In general, a statement involving the *n* variables $\color{red}x_{1},x_{2},...,x_{n}$ can be denoted by $\color{red}P(x_{1},x_{2},...,x_{n})$

A statement of the form $P(x_{1},x_{2},...,x_{n})$ is the value of the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|propositional]] function $\color{red}P$ at the *n*-tuple $\color{red}(x_{1},x_{2},...,x_{n})$, and $P$ is also called an $\color{red}\text{\emph{n}-ary predicate}$

### Quantification
| Type | Statement | When True? | When False? |
| :-- | :-- | :-- | :-- |
| [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Quantification/Universal Quantification\|Universal]] | $\forall x\ P(x)$ | $P(x)$ is true for every $x$ | There is an $x$ for which $P(x)$ is false |
| [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Quantification/Existential Quantification\|Existential]] | $\exists x\ P(x)$ | There is an $x$ for which $P(x)$ is true | $P(x)$ is false for every $x$ |
#### [[De Morgan's Laws\|De Morgan's Laws]] for Quantifiers
|Type | [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Negation\|Negation]] | Equivalent | When is [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Negation\|negation]] true? | When false? |
| :-: | :-: | :-: | :-: | :-: |
|[[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Negating Quantification/Negating an Existential Quantification\|Existential]]|$\neg{\exists x\ P(x)}$|$\forall x\ \neg{P(x)}$| For every $x$, $P(x)$ is false | There is an $x$ for which $P(x)$ is true |
|[[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Negating Quantification/Negating a Universal Quantification\|Universal]]|$\neg{\exists x\ P(x)}$|$\neg{\forall x\ P(x)}$|$\exists x\ \neg{P(x)}$| There exists an $x$, for which $P(x)$ is false | $P(x)$ is true for every $x$ |
#### Precedence
The quantifiers $\forall$ and $\exists$ have higher precedence than all logical operators from [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|propositional logic]]

For example, $\forall x\ P(x) \lor Q(x)$ is the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Disjunction\|disjunction]] of $\forall x\ P(x)$ **and** $Q(x)$
In other words, it means $\textcolor{red}{(}\forall x\ P(x)\textcolor{red}{)} \lor Q(x)$
#### Nested Quantifiers
Everything within the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Free and Bound Variables#^Scope\|scope]] of a quantifier can be thought of as a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|propositional]] function. For example,
$$
\color{red}
\forall x\ \exists y\ (x+y=0)
$$
expresses the same as
$\color{red} \forall x\ Q(x)$, where $\color{lightgreen} Q(x)$ is $\color{lightgreen} \exists y\ P(x,y)$, where $\color{blue} P(x,y)$  is $\color{blue} x+y=0$

$\color{red} \text{Important}$: For each variable that is quantified we need to specify the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|domain]]. Different variables can have different [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|domains]]

#TODO Slightly more to do, up to page 22
