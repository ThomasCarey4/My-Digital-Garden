---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/discrete-mathematics/3-graph-theory/theorems/corollary-3-2/","tags":["Theorem"]}
---

A [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Connected Graph\|connected graph]] $G$ has a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Euler path\|Euler path]] [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Biconditional\|if and only if]] it has exactly two vertices of odd degree
{ #Def}


###### *Proof*
Let $G$ be a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Connected Graph\|connected graph]]

$(\implies)$ Suppose that $G$ has a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Euler Cycles\|Euler path]] $P$ that begins at $u$ and ends at $v$, $u\neq v$. Each time a vertex occurs as an internal vertex of $P$, two of the edges incident to it are used. Since $P$ contains every edge of $G$, it follows that $u$ and $v$ have odd degree, and the remaining vertices have even degree.

$(\impliedby)$ Suppose that $G$ has exactly two vertices $u$ and $v$ of odd degree. Let $G'$ be a graph obtained from $G$ by adding a new edge ${\color{yellow} e}$ between $u$ and $v$. Note that $G’$ is connected and has at least one edge. Also, in $G'$ all vertices have even degree. By [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Theorems/Theorem 3.2\|Theorem 3.2]], $G'$ contains a Euler cycle $C$. Then by removing ${\color{yellow} e}$ from $C$ we get a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Euler path\|Euler path]].