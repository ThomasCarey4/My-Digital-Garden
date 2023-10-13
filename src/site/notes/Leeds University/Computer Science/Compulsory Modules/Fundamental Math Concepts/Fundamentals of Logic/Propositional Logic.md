---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/propositional-logic/","tags":["TODO"]}
---

>[!Textbook Reference]
> [Discrete Mathematics and Its Applications](https://leeds.primo.exlibrisgroup.com/permalink/44LEE_INST/13rlbcs/alma991019654648905181) - 1.1

A proposition is a declarative statement - objectively true or false, not both.
Variables in propositional logic must be constant - e.g. cannot use time or place.
T > True
F > False
### Connectives
- 'not' | $\neg$  - Negation
- 'and' | $\land$ - Conjunction
- 'or' | $\lor$  - Disjunction
- 'if... then' | $\rightarrow$ - Implication \{$Hypothesis \rightarrow Conclusion$}
- 'if and only if' | $\leftrightarrow$ - Biconditional (Its XAND)
#### Implication
$Hypothesis$ can only be true if the $conclusion$ is true, but there is ***no*** guarantee

| p | q | p $\rightarrow$ q |
|:-:|:-:|:------:|
| T | T | T | 
| T | F | F |
| F | T | T |
| F | F | T |
###### Converse
- The converse of $p \rightarrow q$ is $q \rightarrow p$
###### Contrapositive
- The contrapositive of $p \rightarrow q$ is $\neg p \rightarrow \neg p$ 
Can be shown as $( \neg p \lor q )$
#### Biconditional
| p | q | p $\leftrightarrow$ q |
|:-:|:-:|:------:|
| T | T | T | 
| T | F | F |
| F | T | F |
| F | F | T |
**If $Hypothesis = Conclusion$ then true**
- Can be written as " p iff q " 


### Syntax Trees

An illustrated view of the structure of a formula

**Example tree:** $( p \lor q) \land (\neg p \rightarrow r)$
#TODO
### More Definitions

- **Truth Assignment** - Basically just a a row in a truth table
- **Tautology** - A formula that is true under every truth assignment
- **Contradiction** - A formula that is false under every truth assignment
- **Contingency** - Any other formula (Neither a **tautology** or **contradiction**)

### Logical Equivalence
*Formulas that have the same truth value under all possible truth assignments
are logically equivalent*
$p \equiv q$ 