---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/fundamental-math-concepts/fundamentals-of-logic/propositional-logic/laws/","tags":["TODO"]}
---

#### Equivalency with Brackets
##### Idempotent Law
$$ ( p \land p ) \equiv p $$
$$ ( p \lor p ) \equiv p $$
##### Commutative Law
$$ ( p \land q ) \equiv ( q \land p )$$
$$ ( p \lor q ) \equiv ( q \lor p )$$
##### Associative Law
$$ ( p \land q ) \land r \equiv p \land ( q \land r )$$
$$ ( p \lor q ) \lor r \equiv p \lor ( q \lor r )$$
##### Absorption Law
$$ p \land ( p \lor q ) \equiv p$$
$$ p \lor ( p \land q ) \equiv p$$
##### Distributive Law
$$ p \land ( q \lor r ) \equiv ( p \land q ) \lor ( p \land r ) $$
$$ p \lor ( q \land r ) \equiv ( p \lor q ) \land ( p \lor r ) $$
##### Double Negation
$$ \neg \neg p \equiv p $$
##### [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/De Morgan's Law\|De Morgan's Law]]
$$ \neg ( p \land q ) \equiv ( \neg p \lor \neg q ) $$
$$ \neg ( p \lor q ) \equiv ( \neg p \land \neg q ) $$
##### Tertium Non Datur
$$ ( p \land \neg p ) \equiv \textbf{F} $$
$$ ( p \lor \neg p ) \equiv \textbf{T} $$
##### Identity Law
$$ ( p \land \textbf{T} ) \equiv p $$
$$ ( p \lor \textbf{F} ) \equiv p $$
##### Domination Law
$$ ( p \lor \textbf{T} ) \equiv \textbf{T} $$
$$ ( p \land \textbf{F} ) \equiv \textbf{F} $$
#TODO -- Theorem 2.26, Lecture 4
#### Equivalences using Biconditional Statements
1. $p \leftrightarrow q \equiv ( p \rightarrow q) \land (q \rightarrow p)$
2. $p \leftrightarrow q \equiv \neg p \leftrightarrow \neg q$
3. $p \leftrightarrow q \equiv ( p \land q ) \lor ( \neg p \land \neg q )$
4. #TODO 

