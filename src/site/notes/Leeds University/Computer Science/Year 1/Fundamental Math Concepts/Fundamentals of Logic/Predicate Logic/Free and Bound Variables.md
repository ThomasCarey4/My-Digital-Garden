---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/fundamental-math-concepts/fundamentals-of-logic/predicate-logic/free-and-bound-variables/"}
---

When a quantifier is used on the variable $x$, we say that this occurrence of the variable is $\color{red}\text{bound}$

An occurrence of a variable that is not bound by a quantifier or [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] equal to a particular value is said to be $\color{red} \text{free}$

If all the variable that occur in a [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Free and Bound Variables#Predicate and Propositional Logic Propositional Functions\|predicate function]] are $\color{red} \text{bound}$, then that is called a $\color{red} \text{sentence}$ of predicate logic
{ #Sentence}


This can be done using a combination of universal quantifiers, existential quantifiers, and value assignments

The part of a logical expression to which a quantifier is applied is called the $\color{red} \text{scope}$ of this quantifier. Consequently, a variable is free if it is outside the scope of all quantifiers in the [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|Formula]] that specify this variable
{ #Scope}


#### For Example
1. $\exists x\ (P(x) \land Q(x)) \lor \forall x\ R(x)$
	- The variable x is bound. It occurs within the ***scope*** of $\exists$ in the first part of the [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Disjunction\|Disjunction]], and within in the scope of $\forall$ in the second part
2. $\forall x\ (P(y) \land Q(x)) \lor \forall y\ R(y)$
	- The variable $x$ is bound. It occurs within the scope of $\exists$ in the first part of the [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Disjunction\|Disjunction]]. The variable $y$ occurs both as free ( In the first part ) and as bound ( Within the scope of $\forall$ in the second part )