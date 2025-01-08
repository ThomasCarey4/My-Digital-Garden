---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/software-eng-principles/revision/l4-requirements-engineering/"}
---


##### **Two ways:**
**Waterfall/Plan-driven**
- Big document of (unchanging) requirements
**Agile**
- Iterating prototypes and ask the stakeholders what they want to add/remove
##### **Ways of writing a system requirements spec.**

**Natural Language**
- Just writing it using numbered sentences, each sentence should express one requirement
**Structured Natural Language**
- Similar to ‘Natural Language’ but uses a standard form template
**Design Description Languages**
- Pseudo code-like  language used to specify the requirements by defining an operational model of the system. This is rarely used
**Graphical Notations**
- Graphical models, supplemented by text annotations; like UML and sequence diagrams
**Mathematical Specifications**
- Just use maths and LaTeX, rarely used as it can be hard for customers to understand
***
##### **Stakeholder**
- Any person or organisation who is affected by the system in some way and so who has a legitimate interest. A class (or group) of people or organisations who **”hold a stake**
- Don’t have to directly interact with the software or system, only affected by them
##### User Stories
Common structure:
> **As a** [user] … **I want to** … **so that** ...

Be sure to write the story from the perspective of the user, *don’t* specify what the system is doing on the backend, to allow for design flexibility.
##### Use Cases
Ensure to use ambiguous/abstract words to allow for flexibility.
![usecase.png|600](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/usecase.png)
![usecase2.png|600](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/usecase2.png)
Sales Manager *inherits* **from** Sales Coordinator

Use cases model the functions that are required **without** saying how they will be done
- Thinking about requirements starts from a position of “standing outside” of the system and deciding what is needed by the user, ***without*** knowing anything about the detail inside
###### Value Proposal
People are *lazy*!
- A value proposal is a clear statement of what **reward** (or value) is proposed to make the required effort worthwhile
$$
{\color{lightgreen}\text{Reward}}{\color{red}\ >>\ }\text{Effort}
$$
![usecase3.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/usecase3.png)
>[!tip] 
>An arrow means the communication is one way, and output from the system that goes to another actor, for example a data interface to another system

System actors (secondary actors) are other systems that the primary system interacts with that don’t directly interface with the user. Could be simply a piece of software or a system that is not necessary to be shown in the specific use case.