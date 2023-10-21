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
\textrm{and}
$$
$$
\color{lightgreen}\textrm{Computer }x\textrm{ is under attack by an intruder}
$$
$$
\textrm{and}
$$
$$
\color{lightgreen}\textrm{Computer }x\textrm{ is functioning properly}
$$
are often found in mathematical assertions, in computer programs, and in system specifications.

These statements are neither true nor false when the values of the variables are not specified
### Predicate and [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|Propositional]] Functions
The statement $\textquoteleft\color{red}x\color{lightgreen}\textrm{ is greater than 3}\color{white}\textquoteright$ has two parts
$\color{red}\boxed{O}$ = The variable $\color{red}x$, is the ***subject*** of the statement
$\color{lightgreen}\boxed{O}$ = The ***predicate*** $\color{lightgreen}\textquoteleft\textrm{is greater than 3}\textquoteright$, refers to *a property that the subject of the statement **may or may not have***

We can denote the statement $\textquoteleft\color{red}x\color{lightgreen}\textrm{ is greater than 3}\color{white}\textquoteright$ by $\color{red}P(x)$, where *P* denotes the predicate 'is greater than 3' and $x$ is the variable

The statement *$P(x)$* is also said to be the value of the $\color{red}\textrm{propositional function}$ *$P$* and $x$

Once a value has been assigned to the variable $x$, the statement $P(x)$ becomes a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|proposition]] and has a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Truth Value\|truth value]]

#### More Than One Variable?
We can also have statements that involve more than one variable. For instance, consider the statement $\color{red}x=y+3$

We can denote this statement by $\color{red}Q(x,y)$, where $x$ and $y$ are variables and $\color{red}Q$ is the predicate

Once values are assigned to the variables $x$ and $y$, the statement $\color{red}Q(x,y)$ becomes a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|proposition]] and has a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Truth Value\|truth value]]

### *n*-ary Predicates
In general, a statement involving the *n* variables $\color{red}x_{1},x_{2},...,x_{n}$ can be denoted by $\color{red}P(x_{1},x_{2},...,x_{n})$

A statement of the form $P(x_{1},x_{2},...,x_{n})$ is the value of the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic\|propositional]] function $\color{red}P$ at the *n*-tuple $\color{red}(x_{1},x_{2},...,x_{n})$, and $P$ is also called an $\color{red}\textrm{\emph{n}-ary predicate}$

 
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/predicate-logic/sets/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




#### Notation
$\color{red} x \in A$ denotes that **x is an element** of the set A.
$\color{red} x \notin A$ denotes that **x is not an element** of the set A.
#### Defining Sets
##### By Enumeration
$
\color{lightgreen}A\coloneqq\set{0,1,2,3,4,5}=\set{0,1,2,\bullet\bullet\bullet,5}
$
This is called the **roster method** ( or **extensional** set notation )
##### By characteristic properties
$
\begin{align}
\color{lightgreen}B\coloneqq\set{x\ |\ x\in A\ and\ x\ is\ even}^{1}
\end{align}
$
### Fundamentals
- <span style="color:#ff0000">All elements in a set are distinct.</span>
- <span style="color:#ff0000">The elements of a set do not come with a fixed ordering.</span>
- <span style="color:#ff0000">The same set can be described in different ways.</span>


</div></div>

 ### Quantification
 [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Universal Quantification\|Universal Quantification]]
 [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Existential Quantification\|Existential Quantification]]
 