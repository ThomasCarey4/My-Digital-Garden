---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/software-eng-principles/revision/l3-disciplined-agile-development/"}
---


##### Plan-Driven Development
A plan-driven approach to software engineering is based around separate development stages with the outputs to be produced at each of these stages to be planned in advance.
- Iteration occurs *within* activities
![plan-based devlopment.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/plan-based%20devlopment.png)
##### Agile Development
Specification, design, implementation and testing are inter-leaved and the outputs from the development process are decided through **a process of negotiation** during the software development process.
- Program specification, design, implementation are inter-leaved
- The system is developed as a series of version or increments with stakeholders involved in version specification and evaluation
- Frequent delivery of new version for evaluation
- Extensive tool support (e.g. automated testing tools) used to support development
- Minimal documentation — focus on making working code
![agile devlopment.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Software%20Eng%20Principles/Revision/images/agile%20devlopment.png)
##### Agile Manifesto
1. Our highest priority is to satisfy the customer through early and continuous delivery of valuable software
2. Welcome changing requirements, even late in development. Agile processes harness change for the customer’s competitive advantage
3. Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale
4. Business people and developers must work together daily throughout the project
5. Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done
6. The most efficient and effective method of conveying information to and within a development team is face-to-face conversation
7. Working software is the primary measure of progress
8. Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain constant pace indefinitely
9. Continuous attention to technical excellence and good design enhances agility
10. Simplicity–the art of maximising the amount of work not done–is essential
11. The best architectures, requirements and designs emerge from self–organising teams
12. At regular intervals, the team reflects on how to become more effective, then tunes and adjusts its behaviour accordingly

**Let’s talk to each other**
**Let’s just build it and show you**
**Let’s trust each other**
**Let’s respond to what is happening and what we learn**

##### eXtreme Programming (XP)
A very influential agile method, developed in the late 1990’s, that introduced a range of agile development techniques. Extreme Programming (XP) takes an ‘extreme’ approach to iterative development
- New versions may be built several times per day
- Increments are delivered to customers every 2 weeks
- All tests must be run for every build and the build is only accepted if tests run successfully
**Incremental planning**
- Requirements are recorded on story cards and the stories to be included in a release are determined by the time available and their relative priority. The developers break these stories into development ‘Tasks’
**Small releases**
- The minimal useful set of functionality that provides business value is developed first. Releases of the system are frequent and incrementally add functionality to the first release
**Simple design**
- Enough design is carried out to meet the current requirements and no more
**Test-first development**
- An automated unit test framework is used to write tests for a new piece of functionality before that functionality itself is implemented
**Refactoring**
- All developers are expected to refactor the code continuously as soon as possible code improvements are found. This keeps the code simple and maintainable.
**Pair programming**
- Developers work in pairs, checking each other’s work and providing the support to always do a good job
**Collective ownership**
- The pairs of developers work on all areas of the system, so that no islands of expertise develop and all the developers take responsibility for all the code. Anyone can change anything.
**Continuous integration**
- As soon as the work on a task is complete, it is integrated into the whole system. After any such integration, all the unit tests in the system must pass
**Sustainable pace**
- Large amounts of overtime are not considered acceptable as the net effect is often to reduce code quality and medium term productivity
**On-site customer**
- A representative of the end-user of the system (the customer) should be available full time for the use of the XP team. In an extreme programming process, the customer is a member of the development team and is responsible for the bringing system requirements to the team for implementation
##### Scrum
Sprints are fixed length, normally 2–4 weeks.
Fast, “sprints” of coding where the team is isolated from the customer and the organisation, with all the communications channelled through the so called ‘Scrum master’.
The role of the Scrum master is to protect the development team from external distractions. At the end of the sprint, the work done is reviewed and presented to stakeholders. The next sprint cycle then begins.

**Development team**
- A self-organising group of software developers, which should be no more than 7 people. They are responsible for developing the software and other essential project documents
**Potentially  shippable product increment**
- The software increment that is delivered from a sprint. The idea is that this should be ‘potentially shippable’ which means that it is in a finished state and no further work, such as testing, is needed to incorporate it into the final product. In practice, this is not always achievable
**Product backlog**
- This is a list of ‘to do’ items which the Scrum team must tackle. They may be feature definitions for the software, software requirements, user stories or descriptions of supplementary tasks that are needed, such as architecture definition or user documentation
**Product owner**
- An individual (or possibly a small group) whose job is to identify product features or requirements, prioritise these for development and continuously review the product backlog to ensure that the project continues to meet critical business needs. The Product Owner can be a customer but might also be a Product Manger in a software company or other stakeholder representative
**Scrum**
- A daily meeting of the Scrum team that reviews progress and prioritises work to be done that day. Ideally, this should be a short face-to-face meeting that includes the whole team
**Scrum Master**
- The Scrum Master is responsible for ensuring that the Scrum process is followed and guides the team in the effective use of Scrum. He or she is responsible for interfacing with the rest of the company and for ensuring that the Scrum team is not diverted by outside interference. The Scrum developers are adamant that the Scrum Master should not be thought of as a project manager. others, however, may not always find it easy to see the difference.
**Sprint**
- A development iteration. Sprints are usually 2–4 weeks long
**Velocity**
- An estimate of how much product backlog effort that a team can cover in a single sprint. Understanding a team’s velocity helps them estimate what can be covered in a sprint and provides a basis for measuring improving performance.
##### Incident logging
Similar to Kanban, but for live systems, where users provide tasks for the backlog.

##### DevOps
(ideally) Fully automated testing