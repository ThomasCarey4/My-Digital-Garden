---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/discrete-mathematics/3-graph-theory/theorems/lemma-3-2/","tags":["Theorem"]}
---

Every odd [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Closed Path\|closed path]] contains an odd [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|simple cycle]]
{ #Def}


###### *Proof*
Suppose $C$ is an odd closed path. We prove the result by induction on the length $l$ of $C$.

**Base Case**: If $l=1$, then $C$ is a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Loop\|loop]], which is a [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|simple cycle]] of length 1

**Induction Step**: Suppose $l>1$ and the claim holds for all odd closed paths of length less than $l$ (this is the induction hypothesis). 
If $C$ has no repeated vertices (other than first $=$ last), then $C$ is an odd [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|simple cycle]]. If vertex $v$ is a repeated vertex in $C$, then we can partition $C$ into two [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Closed Path\|closed paths]] from $v$ to $v$, say $C_{1}$ and $C_{2}$. Since $C$ is odd, $C_{1}$ or $C_{2}$ must be odd. 
Without loss of generality, $C_{1}$ is odd.
Since $C_{1}$ is odd, and of length less than the length of $C$, by induction hypothesis, $C_{1}$ contains an odd [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|simple cycle]] and hence so does $C$

**Note** that it is not true that every even closed path contains an even [[Leeds University/Computer Science/Year 1/Discrete Mathematics/3. Graph Theory/Definitions/Def. Cycle\|simple cycle]]
