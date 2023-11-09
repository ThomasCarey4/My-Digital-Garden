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
An illustrated view of the structure of a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]]

**Example tree:** $( p \lor q) \land (\neg p \rightarrow r)$
![Syntax Tree.png](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Fundamental%20Math%20Concepts/Fundamentals%20of%20Logic/Propositional%20Logic/Syntax%20Tree.png)
### More Definitions


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/definitions/truth-assignment/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




A truth assignment is a possible outcome of a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]], and the variables necessary for said outcome.
- A common example is a row in a truth table


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/definitions/tautology/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




A [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] that is true under every [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Truth Assignment\|truth assignment]].

</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/definitions/contradiction/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




A [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] that is false under every [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Truth Assignment\|truth assignment]].

</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/definitions/contingency/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




A [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] that is neither a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Tautology\|Tautology]] or a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Contradiction\|Contradiction]].

</div></div>


### [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Logical Equivalence\|Logical Equivalence]]
*[[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|Formulas]] that have the same [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Truth Value\|truth value]] under all possible [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Truth Assignment\|Truth Assignments]] are logically equivalent*
$p \equiv q$ 

##### Satisfiable
A [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] is called **satisfiable**, if it has any [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Truth Assignment\|Truth Assignments]] that make it true.

A [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] that is not satisfiable is called **unsatisfiable**.

A [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Truth Assignment\|truth assignment]] that makes a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]] true is called a **satisfying assignment** - for that [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Formula\|formula]]
