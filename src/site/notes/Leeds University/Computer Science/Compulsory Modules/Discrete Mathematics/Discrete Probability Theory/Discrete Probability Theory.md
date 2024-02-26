---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/discrete-mathematics/discrete-probability-theory/discrete-probability-theory/"}
---

- An *experiment* is a process that yields an outcome
- The [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|Set]] $\color{red} S$ of all possible outcomes of a given experiment is called the *sample space*
- An *event* $\color{red} A$ is a set of outcomes, i.e. a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/Definitions/Definition 5.5 (Subsets and Supersets)\|Subset]] of the sample space $\color{red} S$

---
**Example**
Experiment: Rolling a six-sided die
Sample Space: $\color{lightgreen} S = \set{1,2,3,4,5,6}$
Event: Obtaining a 4 when rolling a die, i.e. $\color{lightgreen} A= \set{4}$

Since an event is a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|Set]], we can combine events to form new events using various [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|Set]] operations
1. $\color{lightgreen} A \cup B$ is the event that occurs [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Biconditional\|if and only if]] $\color{lightgreen} A$ occurs **or** $\color{lightgreen} B$ occurs (or both)
2. $\color{lightgreen} A \cap B$ is the event that occurs [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Biconditional\|if and only if]] $\color{lightgreen} A$ occurs **and** $\color{lightgreen} B$ occurs
3. $\color{lightgreen} \bar{A}$, the complement of $\color{lightgreen} A$, is the event that occurs [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Biconditional\|if and only if]] $\color{lightgreen} A$ does **not** occur

---
**Example**
Let $\color{lightgreen} A$ be the event that an even number occurs, $\color{lightgreen} B$ that an odd number occurs, $\color{lightgreen} C$ that a prime number occurs

$A=\set{2,4,6},\ B=\set{1,3,5},\ C=\set{2,3,5}$
$A \cup C=\set{2,3,4,5,6}$ the even that an **even** or a **prime number** occurs
$B \cap C=\set{3,5}$ the even that an **odd prime number** occurs
$\bar{C}=\set{1,4,6}$ the event that a prime number does not occur
A and B are *mutually exclusive*
