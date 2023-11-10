---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/proof-techniques/equivalence-proofs/"}
---

##### [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Proof Techniques/Definitions/Theorem\|Theorem]] 4.5
*If* $n$ *is a positive integer, then* $n$ *is odd [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Biconditional\|if and only if]]* $n^{2}$ *is odd*
###### Proof
Let $n$ be a positive integer. We prove the following two parts;
1. If $n$ is odd, then $n^{2}$ is odd
2. If $n^{2}$ is odd, then $n$ is odd
Proof of 1: This follows from [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Proof Techniques/Theorems/Theorem 4.2\|Theorem 4.2]]
Proof of 2: We proceed by [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Proof Techniques/Proof by Contraposition\|contraposition]], i.e. assuming that $n$ is even, we want to show that then $n^{2}$ is even. Since $n$ is even, we have $n=2\ell$ for some integer $\ell$. Hence
$$
n^{2} = (2\ell)^{2} = 4\ell^{2} = 2(2\ell^{2})
$$
Hence, by definition of 'even', $n^{2}$ is even. This proves part 2.
Together, parts 1 and 2 prove the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Proof Techniques/Definitions/Theorem\|theorem]]
