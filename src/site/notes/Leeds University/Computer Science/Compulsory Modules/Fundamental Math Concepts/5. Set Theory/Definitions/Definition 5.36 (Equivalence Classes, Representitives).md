---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/5-set-theory/definitions/definition-5-36-equivalence-classes-representitives/","tags":["Definition"]}
---

Let $E$ be an [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.34 (Equivalence Relations)\|equivalence relation]] over a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] $V$.
For every $v \in  V$ we let$$
\color{red} [v]_{E} \coloneqq \set{v' \in V\ |\ (v, v') \in E}
$$denote the $\color{red}\text{equivalence class of}$ $v$ with respect to $E$ $\color{lightgreen}\text{(i.e. the equivalence class }[V]_{E}\text{ consists of all elements of }V$
$\color{lightgreen}\text{that are }\textquoteleft\text{equivalent}\textquoteright\text{ to }v\text{ according to }E\text{).}$
A [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] $W \subseteq V$ is an $\color{red}\text{equivalence class}$ (of $E$), if there exists an element $v \in V$ with $W = [v]_{E}$
The element $v$ is then called a $\color{red}\text{representative}$ of its equivalence class $W$
{ #def}


>[!example]
>If $V$ is the [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] of all people and $E$ is the "having the same age" [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]], then an equivalence class $W$ would be the group of all people who are the same age as $v$. This $W$ would be an equivalence class because it contains all individuals who share the same age as person $v$
### Orders

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/5-set-theory/definitions/definition-5-37/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




Let $E$ be a binary [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.4 Relations\|relation]] over a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] $V$.
1. $E$ is a $\color{red}\text{preorder}$, if $E$ is [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.37 (Reflexive)\|reflexive]] ***and*** [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.39 (Transitive)\|transitive]]
2. $E$ is a $\color{red}\text{partial order}$, if $E$ is [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.37 (Reflexive)\|reflexive]], [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.39 (Transitive)\|transitive]] ***and*** [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.38.2 (Antisymmetric)\|antisymmetric]]
3. $E$ is a $\color{red}\text{linear order}$ or [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.41 (Total)\|total]] $\color{red}\text{order}$, if $E$ is [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.37 (Reflexive)\|reflexive]], [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.39 (Transitive)\|transitive]], [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.38.2 (Antisymmetric)\|antisymmetric]] ***and*** [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.41 (Total)\|total]]


</div></div>

