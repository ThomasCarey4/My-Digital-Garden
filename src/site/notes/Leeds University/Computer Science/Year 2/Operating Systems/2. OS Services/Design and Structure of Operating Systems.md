---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/2-os-services/design-and-structure-of-operating-systems/"}
---


The internal structure can vary widely, based on the purpose of the OS
**User goals** and **system goals** first are outlined

**User**: Easy to learn and use, reliable, fast, safe
**System**: Easy to design, implement and maintain; efficient, reliable and error free

###### Policy and Mechanism
The separation of **policies** (what) and **mechanisms** (how) is an important concepts
- **Example policy**: Interrupt the OS regularly; **Mechanism**: Timer interrupts
- This is a good approach as we can change policies later and mechanisms are in place: For example, you can change the timer interrupt frequency

>[!example]  Linux Example
>The standard Linux kernel has a specific CPU scheduler—but we can change it to support a different policy in how we schedule different jobs on the systme
Mechanism

###### Languages
The OS is a collection of many programs, implemented by many people over years—general statements are hard to make but there are some common points
- **Kernel**: assembly, C
- **Higher level routines**: C, C++, other
- For example, Android is mostly C and some assembly
	- **System libraries**: C or C++
	- **APIs**: Java

>[!info] Advantages of High Level Languages
>The code is written faster, more compact, easier to understand and maintain. Compiler improvements are easy to integrate by recompiling the OS. Easier to port the whole OS to new architectures
>

>