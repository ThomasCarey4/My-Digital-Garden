---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/propositional-logic/propositional-logic/"}
---

>[!Textbook Reference]
> [Discrete Mathematics and Its Applications](https://leeds.primo.exlibrisgroup.com/permalink/44LEE_INST/13rlbcs/alma991019654648905181) - 1.1

A proposition is a declarative statement - objectively true or false, not both.
Variables in propositional logic must be constant - e.g. cannot use time or place.
T > True
F > False
### Connectives
- 'not' | $\neg$  - [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Negation\|Negation]]
- 'and' | $\land$ - [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Conjunction\|Conjunction]]
- 'or' | $\lor$  - [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Disjunction\|Disjunction]]
- 'if... then' | $\rightarrow$ - [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Implication\|Implication]] \{$Hypothesis \rightarrow Conclusion$}
- 'if and only if' | $\leftrightarrow$ - [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Biconditional\|Biconditional]] (Its XAND)

### Syntax Trees
An illustrated view of the structure of a formula

**Example tree:** $( p \lor q) \land (\neg p \rightarrow r)$
![Syntax Tree.png](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Fundamental%20Math%20Concepts/Fundamentals%20of%20Logic/Propositional%20Logic/Syntax%20Tree.png)
### More Definitions

- **Truth Assignment** - Basically just a a row in a truth table
{ #Truth-Assignment}

- **Tautology** - A formula that is true under every truth assignment
{ #Tautology}

- **Contradiction** - A formula that is false under every truth assignment
{ #Contradiction}

- **Contingency** - Any other formula (Neither a **tautology** or **contradiction**)
{ #Contingency}


### [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Logical Equivalence\|Logical Equivalence]]
*Formulas that have the same truth value under all possible truth assignments are logically equivalent*
$p \equiv q$ 

##### Satisfiable
A formula is called **satisfiable**, if it has [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Propositional Logic#^Truth-Assignment\|truth assignment]] that makes it true.

A formula that is not satisfiable is called **unsatisfiable**.

A truth assignment that makes a formula true is called a **satisfying assignment** - for that formula

