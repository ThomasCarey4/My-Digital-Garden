---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/5-set-theory/definitions/definition-5-39-transitive/","tags":["Definition"]}
---

A [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]] $R$ on a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] $A$ is called $\color{red}\text{transitive}$ if whenever $(a, b) \in R$ and $(b, c) \in R$, then $(a, c) \in R$, for all $a, b, c \in A$
{ #def}


>[!example] 
>If we consider the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]] $R$ that contains $(x, y)$ if $x$ is older than $y$ on the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] of all students in the class, then we know that if $(x, y) \in R$ and $(y, z) \in R$, then $(x, z) \in R$

>[!tip] 
>This can be formalised in [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Predicate Logic/Predicate Logic\|predicate logic]] by
>$$\color{lightgreen} \forall x \forall y \forall z (((x, y) \in R \land (y, z) \in R) \to (x, z) \in R)$$
>Where the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.27.1 (Domain, Codomain)\|domain]] is the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] of all elements in $A$



