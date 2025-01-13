---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/software-eng-principles/revision/l8-uml-boot-camp/"}
---


***UML***:
- $\color{red}\textbf{U}$nified
- $\color{lightgreen}\text{M}$odelling
- $\color{blue}\text{L}$anguage

The Unified Modelling Language (UML) is a language for specifying, visualising, constructing and documenting the artefacts of software systems, as well as for business models and other non-software systems. The UML represents a collection of best engineering practices that have proven successful in the modelling of large and complex systems.

UML can be:
- **Concept Level** - High-level, only the most basic information
![UML-ConceptLevel.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-ConceptLevel.png)
- **Design Level** - Low-level, all the information
![UML-DesignLevel.png|300](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-DesignLevel.png)

>[!important] $7\pm2$ Rule
>Typically a UML diagram should only contain between 5 and 9 elements of the same type

#### Use Case Diagrams
Three possible ‘objects’
**System** - A rectangle that contains related Use Cases (***Optional!***)
**Use Case** - An oval that represent an action/sequence of actions that provide something a value to an actor
**Actor** - A stick figure that represents a User that interacts with the Use Cases
**System Actor** - A stick figure that represents an external system, one not covered in the diagram (Must be labelled with <<\?? System>>)

###### Connection Types
- Two-way association: 
  ![usecase-2ass.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/usecase-2ass.png)
- One-way association (This **does not** indicate data flow, only who initiates the interaction)
  ![usecase-1ass.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/usecase-1ass.png)
- Inheritance (Left *inherits from* Right)
  ![usecase-inherit.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/usecase-inherit.png)
###### Rules
- Actors *cannot* directly interact with other actors, but can inherit
- Use Cases *cannot* interact with each other

#### Class Diagrams
**Concept Level**
Sometimes this only shows the class name but the rules are lax.
![class-concept.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/class-concept.png)
Association Notation:
| Class 1 | $a$..$b$ — $c$..$d$ | Class 2 |
An instance of Class 1 can connect to between $c$ and $d$ number of Class 2’s
An instance of Class 2 can connect to between $a$ and $b$ number of Class 1’s
e.g.
| Class 3 | 0..1 — 0..* | Class 4 |
Each Class 3 can connect to any number of Class 4’s (or none)
Each Class 4 can only connect to one Class 3 (or none)

Open arrows are used to show collaboration. For example, above Student is shown to *collaborate with* Enrolment, as a student **must** be able to view their Enrolments, however the Enrolment does not directly reference the Student.

![UML-ClassConcept.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-ClassConcept.png)

Closed arrows show **inheritance** (*Is A* relationships)
Diamonds show **composition** (*Has A* relationships)

**Design Level**
![UML-ClassDesign.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-ClassDesign.png)
Just more info really.

#### Object Diagrams
The same as class diagrams but specific instances and their individual relationships rather than Classes and their general relationships
![UML-Object.png|600](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-Object.png)

#### Collaboration/Communication Diagrams
![UML-Communication.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-Communication.png)
These are Object diagrams with added message arrows to show sequence of the messages sent between collaborating objects for a particular tasks.
#### Sequence Diagrams
Practically the same as Collaboration diagrams:
![UML-Sequence.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-Sequence.png)
Read it top down!
#### Transition Diagrams
Both use the same notation!
![UML-TransitionKey.png|300](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-TransitionKey.png)
Synchronisation bar don’t enforce parallel activities, only that they both have finish before the “flow” can continue.
##### State Diagrams
State diagrams (below) are just flow charts of actions and/or states.
![UML-State.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-State.png)
##### Activity Diagrams
![UML-Activity.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-Activity.png)
These can also be shown with “Swim-lanes” do denote different scopes
![UML-ActivitySwim.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-ActivitySwim.png)
#### Component Diagrams
Component diagrams illustrate the physical structure of the system in terms of its **Software**. They show the software components and the dependencies between them.
![UML-Component.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-Component.png)
An interface (the lollipop) is a publicly accessible class
![UML-ComponentInterface.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-ComponentInterface.png)
#### Deployment Diagram
Deployment diagram illustrates the physical architecture of the system in terms of the **Hardware** it is deployed on and the communication links between hardware nodes.
![UML-Deployment.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-Deployment.png)
Notice the Nodes are specific Objects.
#### Implementation Diagrams
![UML-Implementation.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/UML-Implementation.png)
A mix of both

You can create your own Stereotypes (\<<LAN\>>) for more complicated connections, e.g. \<<TCP/IP\>> or \<<SSL\>>, provided you declare and document them clearly.
