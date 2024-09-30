---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/discrete-mathematics/3-graph-theory/theorems/lemma-3-1/","tags":["Theorem"]}
---

Let $G$ be a graph, and $u$ and $v$ two vertices of $G$. There is a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Path\|path]] from $u$ to $v$ in $G$ [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Biconditional\|if and only if]] there is a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Simple Path\|Def. Simple Path]] from $u$ to $v$ in $G$
{ #Def}


###### *Proof*
Let $u$ and $v$ be vertices of a graph $G$

$(\impliedby)$ A [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Simple Path\|Def. Simple Path]] from $u$ to $v$ in $G$ is a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Path\|Def. Path]] from $u$ to $v$, so the result trivially holds

$(\implies)$ Let $P$ be a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Path\|Def. Path]] from $u$ to $v$. If $P$ has no repeated vertices, then $P$ is a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Simple Path\|simple path]] and we are done. So assume that $P$ has a repeated vertex $w$. Let $P'$ be the [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Path\|Def. Path]] obtained by going along $P$ from $u$ to the first appearance of $w$, and then going along $P$ from the last appearance of $w$ to $v$. So $P'$ is a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Path\|Def. Path]] from $u$ to $v$ whose length is smaller than the length of $P$. If $P'$ has no repeated vertices, then we are done. Otherwise, repeat this procedure. By repeating this procedure until there are no more repeated vertices, we end up with a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Simple Path\|Def. Simple Path]] from $u$ to $v$
