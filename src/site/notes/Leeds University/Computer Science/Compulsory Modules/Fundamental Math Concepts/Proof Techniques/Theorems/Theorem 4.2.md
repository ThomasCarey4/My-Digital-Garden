---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/proof-techniques/theorems/theorem-4-2/","tags":["Theorem"]}
---

*If* $n$ *is an odd integer, then* $n^2$ *is odd.*
$\color{lightgreen}\textrm{Note that the statement of the}$ [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Proof Techniques/Definitions/Theorem\|theorem]] $\color{lightgreen}\text{is of the form}:$
$$
\color{lightgreen} \forall n (P(n)\to Q(n))
$$
$\color{lightgreen}\text{where }P(n)\text{ is }\textquoteleft n \text{ is odd} \textquoteright \text{, } Q(n) \text{ is } \textquoteleft n^{2} \text{ is odd} \textquoteright \text{, with the domain being integers}$
*Remark:* For proving that something is true $\color{red}\text{for all}$ elements of the domain, it is sufficient to prove that the statement is true for an $\color{red}\text{arbitrary}$ element of the domain.
For this we pick a random variable, say, $n$, of the domain, and without making any additional assumptions on $n$, we show that $P(n) \to Q(n)$.
Then, since $n$ could have been any element, we will known that $P(n) \to Q(n)$ is true $\color{red}\text{for all}$ elements of the domain.
###### Proof
Let $n$ be an arbitrary integer, and assume that $n$ is odd. We have to prove that $n^{2}$ is odd.
Since $n$ is odd, there exists an integer $k$ such that $n = 2k + 1$. Squaring both sides of the equation, we obtain
$$
n^{2}=(2k+1)^{2}=4k^{2}+4k+1=2(2k^{2}+2k)+1
$$
Hence, $n^{2}$ can be written as $n^{2}=2\ell + 1$, for an integer $ell$, namely, for the integer $\ell = (2k^{2}+2k)$. Thus, by the definition of an odd integer, we can conclude that $n^{2}$ is an odd integer.
$\color{lightgreen}\text{Note: we started with the assumption ( that }n\text{ is odd ), then made a number}$
$\color{lightgreen}\text{of logical inferences ( }\textquoteleft\text{Since... we obtain...}\textquoteright\text{, }\textquoteleft\text{Hence...}\textquoteright\ \textquoteleft\text{Thus...}\textquoteright\text{ ), until we}$
$\color{lightgreen}\text{arrived at the conclusion}$
