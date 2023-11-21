---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/proof-techniques/proof-by-contraposition/"}
---

In a $\color{red}\text{proof by contraposition}$, a statement of the form $\color{lightgreen}\textquoteleft p \to q \textquoteright$ is proved by showing $\color{lightgreen} \textquoteleft \neg{q} \to \neg{p} \textquoteright$. This is correct, because the statements are logically equivalent
{ #def}


---
##### [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Proof Techniques/Definitions/Theorem\|Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Proof Techniques/Definitions/Theorem]] 4.3
*If* $n$ *is an integer and* $3n+2$ *is odd, then* $n$ *is odd.*
###### Proof
Let $n$ be an arbitrary integer. We proceed by contraposition.
The first step in a proof by contraposition is to assume that the conclusion of the conditional statement $\textquoteleft$If $3n+2$ is odd, then $n$ is odd$\textquoteright$ is false, namely assume that $n$ is even.
Our goal is to how that the premise is false as well, i.e. we want to show that $3n+2$ is even. Since $n$ is even, by definition of an even integer, $n=2k$ for some integer $k$.
Substituting $2k$ for $n$, we find that
$$
3n+2=3(2k)+2=6k+2=2(3k+1)
$$
Hence $3n+2$ is even, because $3n+2 = 2\ell$ for some integer $\ell$, namely for $\ell = (3k+1)$. Thus we have reached our goal and the proof is complete.
$\color{lightgreen}\text{Note: Instead of proving }\textquoteleft p \to q \textquoteright\text{, we proved } \textquoteleft \neg{q} \to \neg{p} \textquoteright\text{.}$
$\color{lightgreen}\text{The proof of } \textquoteleft \neg{q} \to \neg{p} \textquoteright \text{ is a}$ [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Proof Techniques/Direct Proof\|direct proof]]

