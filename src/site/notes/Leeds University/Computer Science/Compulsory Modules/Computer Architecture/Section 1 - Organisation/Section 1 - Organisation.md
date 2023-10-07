---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/section-1-organisation/section-1-organisation/","tags":["#TODO"]}
---

>[!Textbook Reference]
> [Stallings](https://leeds.primo.exlibrisgroup.com/permalink/44LEE_INST/13rlbcs/alma991012536539705181) - 1.1-4, 2.1

*The science and art of selecting and interconnecting components to create computers that meet functional cost and performance goals*

Architecture: the attributes visible to the programmer - software??
	- *Intel x86, ARM64, IBM System/370*
	- Allows for backwards compatibility
1. Instruction set
2. Number of bits used for data representation
3. I/O Mechanisms
4. Addressing Techniques
Organisation: how the architecture is implemented - hardware??
	- Differs between different versions
1. Control signals
2. Interfaces
3. Memory technology

- Computers are very complex, this is simplified by considering a hierarchical structure.
- Each levels the system consists of a set of components and their interrelationships.
- The behaviour at each level depends on a simplified, abstracted characterisation of the system at the next level down.

### Four basic functions of a computer
- Data movement
- Data storage
- Data processing
- Control

### Structural View
#### Top Level
The computer is constructed of:
- Central Processing Unit
- Main Memory
- and Input/Output ports
This is all interfaced via a "Systems Interconnection"
#### CPU
The CPU is constructed of:
- Registers
- an Arithmetic and Logic Unit
- and a Control Unit
This is all interfaced via the "Internal CPU Interconnection"
##### Control Unit
The Control Unit is composed of:
- Sequencing Logic
- and Control Memory
Interfaced together through the "Control Unit Registers and Decoders"

## Summary
- Some parts of the computer are visible to the programmer, some are not
- The majority of today's computers are based on the [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 1 - Organisation/History#Von Neumann Machine\|von Neumann Machine]]
- Architectures are getting more sophisticated in order to increase computing power
- There is inevitably a trade-off between performance and cost