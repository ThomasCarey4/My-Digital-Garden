---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/discrete-mathematics/2-discrete-probability-theory/theorems/theorem-2-2/","tags":["Theorem"]}
---

Let ${\color{red} A}$ and ${\color{orange} B}$ be events. Then $P({\color{red} A}\cup {\color{orange} B})=P({\color{red} A})+P({\color{orange} B})-P({\color{red} A}\cap {\color{orange} B})$
<br>
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/discrete-mathematics/2-discrete-probability-theory/theorems/corollary-2-1/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




If ${\color{red} A}$ and ${\color{orange} B}$ are mutually exclusive events, then $P({\color{red} A}\cup {\color{orange} B})=P({\color{red} A})+P({\color{orange} B})$


</div></div>

{ #Def}


###### *Proof*:
Let ${\color{red} A}=\set{1,2,3,4,5}$
Let ${\color{orange} B}=\set{4,5,6,7}$

$\therefore{\color{red} A}\cup {\color{orange} B}=\set{1,2,3,4,5,6,7}$
$\ \ \ \ {\color{red} A}\cap {\color{orange} B}=\set{4,5}$
However, ${\color{red} A}+{\color{orange} B}=\set{1,2,3,4,{\color{lightgreen}4,5},5,6,7}$
$\implies P({\color{red} A}\cup {\color{orange} B})=P({\color{red} A})+P({\color{orange} B})-P({\color{red} A}\cap {\color{orange} B})$

>[!example] 
>A fair coin is tossed 3 times, and a sequence of heads and tails is observed. What is the probability that an even number of heads **or** at least two tails appear?

${\color{blue} S}=$ The set of sequences of length 3 whose elements are from the set $\set{H,T}$
So $|{\color{blue} S}|=2^{3}=8$
${\color{red} A}=$ The [[Leeds University/Computer Science/Year 1/Discrete Mathematics/2. Discrete Probability Theory/Definitions/Event\|Event]] that an even number of heads appears $= \set{HHT,HTH,THH,{\color{lightgreen} TTT}}$
${\color{orange} B}=$ The [[Leeds University/Computer Science/Year 1/Discrete Mathematics/2. Discrete Probability Theory/Definitions/Event\|Event]] that at least two tails appear $=\set{TTH,THT,HTT,{\color{lightgreen} TTT}}$
${\color{red} A}\cap {\color{orange} B}=$ The [[Leeds University/Computer Science/Year 1/Discrete Mathematics/2. Discrete Probability Theory/Definitions/Event\|Event]] that an even number of heads **and** at least two tails appear $=\set{{\color{lightgreen} TTT}}$
$P({\color{red} A})=\frac{4}{8}=\frac{1}{2},P({\color{orange} B})=\frac{4}{8}=\frac{1}{2},P({\color{red} A}\cap {\color{orange} B})=\frac{1}{8}$
$\implies P({\color{red} A}\cup {\color{orange} B})=P({\color{red} A})+P({\color{orange} B})-P({\color{red} A}\cap {\color{orange} B})=\frac{1}{2} + \frac{1}{2} - \frac{1}{8}=\frac{7}{8}$
