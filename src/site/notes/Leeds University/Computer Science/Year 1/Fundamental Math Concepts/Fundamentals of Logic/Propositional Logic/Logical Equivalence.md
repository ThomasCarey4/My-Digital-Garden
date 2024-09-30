---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/fundamental-math-concepts/fundamentals-of-logic/propositional-logic/logical-equivalence/"}
---

### Conditional
$$
\begin{align*}
p \to q &\equiv \neg{p} \lor q \\
p \to q &\equiv \neg{q} \to \neg{p} \\
p \lor q &\equiv \neg{p} \to q \\
p \land q &\equiv \neg{(p \to \neg{q})} \\
\neg{p \to q} &\equiv p \land \neg{q} \\
(p \to q) \land (p \to r) &\equiv p \to (q \land r) \\
(p \to r) \land (q \to r) &\equiv (p \lor q) \to r \\
(p \to q) \lor (p \to r) &\equiv p \to (q \lor r) \\
(p \to r) \lor (q \to r) &\equiv (p \land q) \to r
\end{align*}
$$
### Biconditional
$$
\begin{align*}
p \leftrightarrow q &\equiv ( p \rightarrow q) \land (q \rightarrow p) \\
p \leftrightarrow q &\equiv \neg p \leftrightarrow \neg q \\
p \leftrightarrow q &\equiv ( p \land q ) \lor ( \neg p \land \neg q ) \\
\neg{(p \leftrightarrow q)} &\equiv p \leftrightarrow \neg{q}
\end{align*}
$$

