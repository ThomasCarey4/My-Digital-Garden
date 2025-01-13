---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/software-eng-principles/revision/l6-advanced-use-cases-realisation/"}
---

Use helicopter method to see the “forest” and get a full view of all the user cases.
![usecase realise.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/usecase%20realise.png)
When realising a Use Case, you need to choose to either use a Use Case Description (Class) or a User Story (Instance). Or both I guess

When modelling a system - start with the actors
Find *at least* one use case for each actor

Determine the **frequency** and **volume** of usage for each use case
- Use this to determine the priorities for USP (i.e. use cases with higher frequency require greater performance)

Uses cases contain:
- **Basic Flow** is the main flow described in the Use Case Description.
- **Alternate Flows** are other variations that still lead to successful completion of the use case. The user still gets measured value.
- **Exception Flows** are variations that lead to an unsuccessful use case - the use fails to complete the use case transaction. The use gets no measurable value.

A Use Case Description can be formatted as a table/forms
UCDForm Template:
```sheet
| Use Case<br>Name: | - | {name} |
| Primary Actor: | - | |
| Other Actors: | - | |
| Value Proposal | - | What do the users get out of this |
| Basic Flow | - | |
| Alternative Flows | - | |
| Exception Flows | - | |
| Assumption | - | e,g. Assume the software system is running |
| Pre-Conditions | - | Any use cases the user must have previously completed |
| Post-Conditions | - | What the user can now do after the use case |
| Non-Functional Requirements | - | e.g. User password is encrypted |
```


##### Business Rules
A business rule is statement that defines or constrains some aspect of the business and which is regarded as fixed for the purpose of process modelling.
**Examples:**
- VAT at 15% **must** be applied to all sales
- All patients **must** have a valid NHS Number 
Business rules are typically set by external legislation or internal strategic management or they may have emerged due to custom and practice. They exist independent of current systems and processes but they **must** be supported by them and changes to business rules are likely to require changes to current systems and practice.

As business rules are liable to change, it is sometimes recommended to maintain a register of business rules – where they can be cross-referenced  in the UCD Form.

Business rules can be conditional, i.e. It is **obligatory** that … *if* …

Rules should have:
- A name
- Use nouns from the business domain model ?
- Specify the degree of authorisation
	- Strict : No exceptions
	- Pre-authorised : Exceptions are allowed with permission beforehand
	- Post-justified : Exceptions *can* be permitted after the violation (not always permitted)
	- Override : Exceptions can be permitted given good reason/excuse
	- Guideline : The rule is simply a suggestion
