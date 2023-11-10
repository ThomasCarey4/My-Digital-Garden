---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/proof-techniques/proof-techniques/"}
---

### Direct Proof

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



In a $\color{red}\textrm{direct proof}$, the statement is proven 'directly', i.e. without any 'detours' 

</div></div>

<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



…often by a chain of implications, leading us from the assumptions of the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Proof Techniques/Definitions/Theorem\|theorem]] to its conclusion; or by a chain of equalities or a chain of equivalences 

</div></div>

### Proof by Contraposition

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/proof-techniques/proof-by-contraposition/#def" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



In a $\color{red}\text{proof by contraposition}$, a statement of the form $\color{lightgreen}\textquoteleft p \to q \textquoteright$ is proved by showing $\color{lightgreen} \textquoteleft \neg{q} \to \neg{p} \textquoteright$. This is correct, because the statements are logically equivalent 

</div></div>

### Proof by Contradiction

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/proof-techniques/proof-by-contradiction/#definition" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



##### Definition
Suppose we want to show a statement of the for $\color{lightgreen} p$ is true. Suppose we find a contradiction $\color{lightgreen} q$ such that $\color{lightgreen} \neg{p} \to q$

Because $\color{lightgreen} q$ is false, but $\color{lightgreen} \neg{p} \to q$ is true, we can conclude that $\color{lightgreen} \neg{p}$ is false, which means that $\color{lightgreen} p$ is true

How can we find a contradiction $\color{lightgreen} q$ that might help us prove that $\color{lightgreen} p$ is true in this way

</div></div>

### Proof by Induction

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/proof-techniques/proof-by-induction/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




By $\color{red} \mathbb{N}$ we denote the set of all $\color{red}\text{natural numbers}$ (i.e. $\mathbb{N} \coloneqq \set{0,1,2,3,...}$)

Let $P(n)$ be a statement about a natural number $n$ The aim is to prove that statement $P(n)$ is true **for every** $n \in \mathbb{N}$. One method to do this is by $\color{red}\text{mathematical induction}$:

1. First, we prove that statement $P(n)$ is true for $n=0$.
    We call this step $\color{red}\text{basis of the induction}$, or simply $\color{red}\text{basis step}$
2. In the second step, we prove for every natural number $n \in \mathbb{N}$:
    **If** statement $P(n)$ is true, **then** the statement $P(n+1)$ is true as well.
    This step is called the $\color{red}\text{inductive step}$

Altogether, this proves that statement $P(n)$ is true $\color{red}\text{for all}$ $n \in \mathbb{N}$


</div></div>

#TODO Proof by cases
#### Common Mistakes
$\color{red}\text{Typical errors}$, that should be avoided when attempting to write a proof, are
- Inadmissible argumentation with examples
- Using the same symbols to denote different things
- Using notations that have not been defined exactly, or even inconsistent definitions
- Inadmissible gaps in the argumentation
- Using unproven claims to justify proof steps
- Thinking that you are finished when there is still something to show
- $\color{red}\text{Circular reasoning}$, i.e. using the statement that you are about to prove in the proof
- Mistakes in arithmetic and basic algebra $\color{lightgreen}\text{( review any troublesome aspects! )}$
#### Existence Proof
How de we proof statements of the form $\color{red} \exists x P(x)$
[[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Proof Techniques/Theorems/Theorem 4.7\|Theorem 4.7]]

