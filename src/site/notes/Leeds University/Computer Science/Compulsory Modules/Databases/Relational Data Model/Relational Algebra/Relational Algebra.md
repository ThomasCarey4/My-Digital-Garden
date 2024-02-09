---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/databases/relational-data-model/relational-algebra/relational-algebra/"}
---

Algebra that *operates* on relations to *define* new relations without changing the operands
##### Basic Operations

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/databases/relational-data-model/relational-algebra/selection/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




$\sigma_{\color{blue} predicate}(\color{lightgreen} R\color{white})$
- Works on a single [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]] $\color{lightgreen} R$ and defines a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]] with [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.14 (Pairs and Tuples)\|tuples]] of $\color{lightgreen} R$ satisfying the condition, the $\color{blue} \text{predicate}$
- $\sigma_{\color{blue} salary > 1000}(\color{lightgreen} Staff\color{white})$


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/databases/relational-data-model/relational-algebra/projection/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




$\Uppi_{\color{blue} col_{1},\dots,col_{n}}(\color{lightgreen} R\color{white})$
- Works on retrieving the attributes from the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]] $\color{lightgreen} R$ with duplicated removed
- $\Uppi_{\color{blue} salary}(\color{lightgreen} Staff \color{white} )$
- $\Uppi_{\color{blue} staffNo,fName,lName,salary}(\sigma_{\color{blue} salary>1000}(\color{lightgreen} Staff \color{white} ))$


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/databases/relational-data-model/relational-algebra/cartesian-product/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




#TODO 

</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/databases/relational-data-model/relational-algebra/union/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




$\color{lightgreen} R \color{red} \cup \color{lightgreen} S$
- The union of two [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relations]] $\color{lightgreen} R$ and $\color{lightgreen}  S$ produces a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]] that contains the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.14 (Pairs and Tuples)\|tuples]] of $\color{lightgreen} R$ or $\color{lightgreen}  S$ or both with duplicates removed
- $\Uppi_{\color{blue} city}({\color{lightgreen} Branch}) \color{red} \cup \color{white} \Uppi_{\color{blue} city}({\color{lightgreen} ProperyForRent})$


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/databases/relational-data-model/relational-algebra/intersection/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




$\color{lightgreen} R \color{red} \cap \color{lightgreen} S$
- Defines a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]] with [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.14 (Pairs and Tuples)\|tuples]] that are in both $\color{lightgreen} R$ and $\color{lightgreen} S$
- $\Uppi_{\color{blue} branchNo}({\color{lightgreen} Branch}) \color{red} \cap \color{white} \Uppi_{\color{blue} branchNo}({\color{lightgreen} Staff})$


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/databases/relational-data-model/relational-algebra/set-difference/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




$\color{lightgreen} R \color{red} - \color{lightgreen} S$
- Defines a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]] of the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.14 (Pairs and Tuples)\|tuples]] that are in [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]] $\color{lightgreen} R$ but not in $\color{lightgreen} S$
- $\Uppi_{\color{blue} branchNo}({\color{lightgreen} Branch}) \color{red} - \color{white} \Uppi_{\color{blue} branchNo}({\color{lightgreen} Staff})$


</div></div>



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/databases/relational-data-model/relational-algebra/theta-join/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




$\color{lightgreen} R \color{red} \bowtie_{\color{blue} F} \color{lightgreen} S$
- Defines a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]] that contains [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.14 (Pairs and Tuples)\|tuples]] satisfying the predicate $\color{lightgreen} F$ from the [[Leeds University/Computer Science/Compulsory Modules/Databases/Relational Data Model/Relational Algebra/Cartesian Product\|Cartesian product]] of $\color{lightgreen} R$ and $\color{lightgreen} S$
- Can be rewritten using basic [[Leeds University/Computer Science/Compulsory Modules/Databases/Relational Data Model/Relational Algebra/Selection\|Selection]] and [[Leeds University/Computer Science/Compulsory Modules/Databases/Relational Data Model/Relational Algebra/Cartesian Product\|Cartesian product]] operations
	- $\color{lightgreen} R \color{red} \bowtie_{\color{blue} F} \color{lightgreen} S \color{white} = \sigma_{\color{blue} F}(\color{lightgreen} R \color{red} \times \color{lightgreen} S \color{white} )$
- If predicate $\color{blue} F$ contains only equality $(=)$, the term **Equijoin** is used


</div></div>

#TODO Finish this
