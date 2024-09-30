---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/discrete-mathematics/3-graph-theory/definitions/def-bipartite-graphs/","tags":["Definition"]}
---

###### Bipartite Graphs
A *bipartite graph* is a graph $G$ whose vertices can be partitioned into two (possibly empty) [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.5 (Subsets and Supersets)\|subsets]] ${\color{blue} X}$ and ${\color{red} Y}$ (so ${\color{blue} X}\cap {\color{red} Y}=\emptyset$ and ${\color{blue} X}\cup {\color{red} Y}={\color{mauve} V}(G)$) such that each edge of $G$ has one end in ${\color{blue} X}$ and one in ${\color{red} Y}$. $({\color{blue} X},{\color{red} Y})$ is called *bipartition* of $G$

Note that a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Simple Graph\|simple graph]] $G$ on one vertex, say $u$ **is** bipartite since we can let ${\color{blue} X}=\set{u}$ and ${\color{red} Y}=\emptyset$.

![Bipartite.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Discrete%20Mathematics/3.%20Graph%20Theory/images/Bipartite.png)


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/discrete-mathematics/3-graph-theory/definitions/def-closed-path/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




A *closed [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Path\|path]]* is a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Path\|path]] that begins and ends at the same vertex. We say that a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Path\|path]] or a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|cycle]] is *even* or *odd* depending on the [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Proof Techniques/Definitions/Parity\|Parity]] of its length.

</div></div>


Note that the graph $G=(\set{u,v},\set{\set{u,v}})$ has a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Closed Path\|closed path]] of positive length (e.g. $u,v,u,v,u$ is [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Closed Path\|closed path]] of $G$ of length 4), but does not have a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|cycle]]

**Lemma 3.2**

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/discrete-mathematics/3-graph-theory/theorems/lemma-3-2/#def" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




Every odd [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Closed Path\|closed path]] contains an odd [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|simple cycle]] 
###### *Proof*
Suppose $C$ is an odd closed path. We prove the result by induction on the length $l$ of $C$.

**Base Case**: If $l=1$, then $C$ is a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Loop\|loop]], which is a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|simple cycle]] of length 1

**Induction Step**: Suppose $l>1$ and the claim holds for all odd closed paths of length less than $l$ (this is the induction hypothesis). 
If $C$ has no repeated vertices (other than first $=$ last), then $C$ is an odd [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|simple cycle]]. If vertex $v$ is a repeated vertex in $C$, then we can partition $C$ into two [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Closed Path\|closed paths]] from $v$ to $v$, say $C_{1}$ and $C_{2}$. Since $C$ is odd, $C_{1}$ or $C_{2}$ must be odd. 
Without loss of generality, $C_{1}$ is odd.
Since $C_{1}$ is odd, and of length less than the length of $C$, by induction hypothesis, $C_{1}$ contains an odd [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|simple cycle]] and hence so does $C$

**Note** that it is not true that every even closed path contains an even [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|simple cycle]]


</div></div>

