---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/software-eng-principles/revision/l13-software-architecture-advanced-principles/"}
---


### Patterns!
Patterns and Pattern Languages are ways to describe best practices, good designs, and capture experience in a way that it is possible for others to reuse this experience.
- A design pattern is a way of reusing abstract knowledge about a problem and its solution
- A pattern is a description of the problem and the essence of its solution
- It should be sufficiently abstract to be reused in different settings
- Pattern description of ten make use of object-oriented characteristics such as standard inheritance and polymorphism.
#### Model-View-Controller (MVC) Pattern
MVC is a very popular pattern (used in ASP .NET) that uses 3 Tier Architecture, i.e. PAD
![Pasted image 20250111211038.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/Pasted%20image%2020250111211038.png)
- **P**resentation $\rightarrow$ Boundary Class $\rightarrow$ View
- **A**pplication $\rightarrow$ Control Class $\rightarrow$ Controller
- **D**ata $\rightarrow$ Entity Class $\rightarrow$ Model
### Transactions
- ***Atomicity*** - Transactions take place completely, or not at all
- ***Consistency*** - Transactions are carried out consistent with pre-determined rules
- ***Isolation*** - Transactions are carried out independent of each other
- ***Durability*** - The effects of a transaction should endure after completion

CRUD!
- **C**reate
- **R**ead
- **U**pdate
- **D**elete
	- Never physically delete anything, only logically delete (simply mark as ‘deleted’), to prevent referential errors

Confirm all important user transactions (i.e. ask the user “Are you sure?”)

Keep an audit record of all/important transactions (extra column(s)) to for easier debugging and accountability (Horizon Post Office scandal!!)

Need valid codes to ensure data is correct (or, valid lol)
- The single data base option (Enterprise or Repository) - **Most Common**
	- Just have one big database on a separate system
- The Federated option
	- Keep the individual databases but store the valid codes behind an API on a separate component
	- Useful in scenarios where systems rarely share data, but still need it to be possible, e.g. hospitals.
