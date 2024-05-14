---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/databases/old/relational-data-model/relational-algebra/theta-join/"}
---

$\color{lightgreen} R \color{red} \bowtie_{\color{blue} F} \color{lightgreen} S$
- Defines a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]] that contains [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.14 (Pairs and Tuples)\|tuples]] satisfying the predicate $\color{lightgreen} F$ from the [[Leeds University/Computer Science/Compulsory Modules/Databases/old/Relational Data Model/Relational Algebra/Cartesian Product\|Cartesian Product]] of $\color{lightgreen} R$ and $\color{lightgreen} S$
- Can be rewritten using basic [[Leeds University/Computer Science/Compulsory Modules/Databases/old/Relational Data Model/Relational Algebra/Selection\|Selection]] and [[Leeds University/Computer Science/Compulsory Modules/Databases/old/Relational Data Model/Relational Algebra/Cartesian Product\|Cartesian Product]] operations
	- $\color{lightgreen} R \color{red} \bowtie_{\color{blue} F} \color{lightgreen} S \color{white} = \sigma_{\color{blue} F}(\color{lightgreen} R \color{red} \times \color{lightgreen} S \color{white} )$
- If predicate $\color{blue} F$ contains only equality $(=)$, the term **Equijoin** is used
