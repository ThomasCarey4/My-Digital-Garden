---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w2-os-services/p4-design-and-structure-of-operating-systems/"}
---


### OS Design and Implementation
The design of an Operating System is a major undertaking and there is no complete solution that could generate an OS automatically when given requirements.
The internal structure can vary widely, based on the purpose of the OS
1. **User Goals** and **System Goals** are first outlined
	1. **User:** Make the OS: Easy to learn and use, reliable, fast, and safe
	2. **System**: make the OS: Easy to design, implement, maintain; efficient, reliable, and error free
$$\boxed{\begin{array}{c}\text{There can be many interpretations of these vague requirements}\end{array}}$$
#### Policy and Mechanism
The separation of **policies** (what) and **mechanisms** (how) is an important concept
- Example **Policy**: Interrupt the OS regularly; 
	- **Mechanism**: Timer interrupts
		- This is a good approach as we can change policies later, but mechanisms are static: For example, we can change the timer interrupt frequency

>[!example] Linux Example
>The standard Linux Kernel has a specific CPU scheduler—but we can change it to support a different policy in how we schedule different jobs on the system

#### Languages
The OS is a collection of many programs, implemented by many people over years—general statements are hard to make by there are some common points:
- **Kernel**: Assembly, C
- **Higher Level Routines**: C, C++, Other

- For example, Android is mostly C and some Assembly
- Android system libraries are C or C++
- Android APIs: Java
>[!abstract] Advantages of High Level Languages
>Code can be written faster, is more compact, and easier to understand and maintain. Compiler improvements are easy to integrate by recompiling the OS. It’s easier to port the whole OS to new architectures

### OS Structure
###### **Monolithic Kernel**:
Place all the functions of the kernel into a single, static binary file that runs a single address space. Not much structure or no structure at all

The original UNIX system used this approach: It had a kernel and the system programs. It has evolved over the years with some structure
![Pasted image 20250119191801.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119191801.png)
Monolithic kernels are simple in concept, but are difficult to implement and extend as everything is in one big kernel rather than structured.

They have a performance advantage, however, which explains why they are still relevant

Monolithic kernels are said to be **tightly coupled** because changes in the system can affect all the other parts

We can instead take a **loosely coupled** approach, where the kernel is structured into parts doing specific and limited things

**Layered system**: The highest layer is the *User Interface*, while the lowest layer is the *Hardware*. Layers can only (directly) call functions from the layer below.

Debugging is easier in this—Debug the first layer without affecting the rest of the system, once done, move up a layer`

###### Microkernel
Kernels can be modularised using the **microkernel** approach

Remove all the nonessential components from the kernel and implement them as User level programs—this results in a small kernel

When the Operating System need to be extended, new services are added in user space rather than modifying the kernel. Kernel modifications require fewer changes since it is so small

It is also easier to port to another OS and provides more security since most services run in user mode

Performance suffers compared to one big kernel—as the different parts have to communicate

![Pasted image 20250119200253.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119200253.png)
