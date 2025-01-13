---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/software-eng-principles/revision/l10-designing-architecture/"}
---


#### Components-based architecture
![architecture.png|600](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/architecture.png)

##### Managing Complexity (Avoiding Spaghetti)
![complexity.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/complexity.png)

Each component should have a **purpose**
Each component should ***internally*  Cohesive** and **provide *external* services** via a limited interface.
Component design is based on applying two of the Four Major Principles of Object Oriented Design
$$
{\color{red}\textbf{Modularity}}\text{ and }{\color{orange}\textbf{Encapsulation}}
$$
**Building with Components** - ${\color{red}\textbf{Modularity}}$
- The property of a system that has been decomposed into a set of cohesive and loosely coupled modules
- ![modularity.png|300](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/modularity.png)

**Building a good Component** - ${\color{orange}\textbf{Encapsulation}}$
- No part of a complex system should be dependent on the internal workings of another part. Encapsulation involves hiding the detail of object attributes and internal operations. Component design extends the concept of encapsulation from classes to a component.
- ![en-cat-sulation.png|300](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/en-cat-sulation.png)

**Useful Components**
are ones that can be used…
- by the developer - to build a working system
- by other team members - to build a working system
- by anyone - to enhance and maintain the system
- by the developer - to build other future systems
- by other team members - to build other future systems
- by anyone - to build other future systems

#### Layered Architecture
One of the founding principles of software design is a layered architecture
Each layer **only** communicates with the layer “above” and the layer “below”
Lower level layers manage physical interactions with networks and hardware
![layered architecture.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/layered%20architecture.png)
##### Three Tier Software Architecture (PAD)
Typically compute systems use a three tier architecture that combines three layers that use different software and different design approaches
1. **P**resentation
	- The user interface (e.g. HTML)
2. **A**pplication
	- An object-oriented development language (e.g. Java, C++)
3. **D**ata
	- A Regional Database Management System (RDBMS) (SQL)

There is often a fourth tier for preparing the **Presentation**, e.g. Python Flask

Typically from the bottom, depending on how detailed your design is.