---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/discrete-mathematics/3-graph-theory/theorems/theorem-3-2/","tags":["Theorem"]}
---

A [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Connected Graph\|connected graph]] with at least one edge has a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Euler Cycles\|Euler cycle]] [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Biconditional\|if and only if]] it has no vertices of odd degree
{ #Def}


###### *Proof*

$(\implies)$ Suppose that $G$ has a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Euler Cycles\|Euler cycle]] $C$ that begins and ends at vertex $v$. Each time a vertex $u$ occurs as an internal vertex of $C$, two of the edges incident to $u$ are used. Since $C$ contains every edge of $G$, $d(u)$ is even for every $u\neq v$. Since $C$ starts and ends at $v$, $d(v)$ is even.

$(\impliedby)$ Assume that $G$ has no vertices of odd degree

**Claim 1**: For every vertex $v\in {\color{mauve} V}(G)$, $G$ contains a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|cycle]] that begins and ends at $v$
*Proof*:
Let $v\in V(G)$. Start building a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Path\|path]] from $v$ (i.e. moving from one vertex to another along the edges), without repeating edges. When the [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Path\|path]] enters a vertex $u\neq v$ through an edge, it can always leave $u$ through an unused edge, since every vertex has an even degree and an odd number of edges incident to $u$ have been used in reaching $u$. So such a walk terminates when we have reached $v$ again, resulting in a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|cycle]].

Let $C$ be a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|cycle]] in $G$ of maximum possible length
**Claim 2**: $C$ is a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Euler Cycles\|Euler cycle]]
*Proof* (by contradiction):
Suppose otherwise, i.e. suppose that ${\color{orange} E}(C)\neq {\color{orange} E}(G)$. Let $G'$ be a subgraph obtained from $G$ by removing the edges in ${\color{orange} E}(C)$. In $G'$ every vertex has even degree. Since $G$ is connected and ${\color{orange} E}(G')\neq \emptyset$, there is at least one edge in ${\color{orange} E}(G')$ that is incident to some vertex $u$ of $C$. By **Claim 1**, $G'$ contains a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|cycle]] $C'$ that begins and ends at $u$. $C$ and $C'$ can be combined into a single [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|cycle]] by breaking apart $C$ at $u$ to include $C'$. This contradicts the choice of $C$, and hence the claim.