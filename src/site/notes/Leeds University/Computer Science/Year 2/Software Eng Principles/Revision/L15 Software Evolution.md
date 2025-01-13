---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/software-eng-principles/revision/l15-software-evolution/"}
---


Greenfield site -> Building a new system without any legacy or old system
Brownfield site -> Building a system on top of/adjacent to another system

![Pasted image 20250112221633.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/Pasted%20image%2020250112221633.png)
**Direct Cutover**:
Just stop the old system and start the new one (typically over the weekend)
- +Efficient
- +Cheap
- -High Risk
**Parallel Running**
Run both systems at the same time
- +Low Risk
- -Difficult
**Phased**
Slowly add the new modules till the old system has been replaced
- +Low Risk
- -Takes a long time
- -Not always compatible
**Pilot**
Slowly rollout across different regions/sites
- +Low Risk
- -Takes a long time

###### Selecting a Changeover method
- **Cost**
- **Time**
- **Quality of the new system** - Is it buggy?
- **Impact on customers** - Do customer service know the new system?
- **Impact on employees** - Do employees need to work extra during the changeover?
- **Technical issues** - Some of the options may not be possible if the system does not have a modular system
### What’s a Legacy System?
Legacy systems are systems that rely on languages and technologies that are no longer used for new system development.
	- It may be dependent on older hardware and may have associated legacy processes and procedures
Legacy systems are not just software systems but are broader socio-technical systems that include hardware, libraries and other supporting software and business processes.
### Types of Maintenance
**Fault repairs**
- Bug fixing
**Environmental Adaptation**
- Adapt the software to a different operating environment (i.e. a new windows version)
**New or Changed Functionality**
- Modifying the system to satisfy new requirements

***Maintenance costs can be 2 to 100 times greater than development cost!***
- Maintenance inevitably corrupts the software structure
- Old languages get more unknown
- Developers leave and the new ones don’t know the code
#### Technical Debt
Technical debt is the implied cost of future reworking because a solution prioritised expedience over long-term design.
	- It’s how much crap code is in a system
This ‘debt’ makes future changes much harder as you stray further away from the initial design.
This massively impacts the evolvability of a system and the cost of maintainability and 

- Duplicate code
- Long methods
- Lots of switch statements
- Data clumping (The same *group* of data appears in multiple places)
- Speculative generality (Redundant code)

###### Refactoring
Improve the structure, design and readability of the code.
Preventative Maintenance!

**When to kill a system?**
When its too expensive to maintain.