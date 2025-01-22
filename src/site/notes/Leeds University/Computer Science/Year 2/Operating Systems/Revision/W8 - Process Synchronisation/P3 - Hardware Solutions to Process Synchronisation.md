---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w8-process-synchronisation/p3-hardware-solutions-to-process-synchronisation/"}
---


### Hardware Support for Synchronisation
**Software-based solutions** fall short in solving the synchronisation problems arising in shared data among threads
>[!hint] 
>A programmer provides code in a certain order; modern architectures reorder this for performance, when there are no data dependencies

#### Memory Barriers
>[!abstract] Memory Model
>How a computer architecture determines what memory guarantees it will provide

There are two memory model categories
1. **Strongly Ordered**: Memory modifications by one processor are known to other processors
2. **Weakly Ordered**: Memory modifications *may not be **immediately*** visible

>[!abstract] Kernel developer assumptions on memory models
>Memory models vary.
>Developers cannot assume what visibility of memory modifications there will be in a shared-memory multiprocessor

Computer architectures solve this issue by including special instructions that ensure any changes made to shared memory (**in cache**) by one processor are made visible to all other processors.

This way all threads running on other processor will know about the memory modifications

>[!abstract] Memory Barriers/Fences
>When a processor meets a **memory barrier**, it makes sure that any memory operations are completed before starting any subsequent ones (even if reordering has been taking place). This way, other threads can see the latest data
>
>Basically, my understanding is that when the programs are reordered, no instructions can cross these barriers—ensuring all code of one section is complete before starting another


#### Hardware Instructions
Modern hardware provides special hardware instructions that allow:
1. **Test-and-modify** the contents of memory
2. **Compare-and-swap** two words of memory
##### Test-And-Set Instruction
![Pasted image 20250122005743.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250122005743.png)
This is a definition of the instruction $\rightarrow$ Implemented in hardware
- These steps happen **atomically—test-and-set** cannot be interrupted
- In a multiprocessor, **test-and-set** also happens sequentially in arbitrary order
	- If `target` stores $1$, we will keep it unchanged
	- If `target` stores $0$, we will return $0$ but change `target` to $1$

**Test-and-set** can be used to implement *[[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W8 - Process Synchronisation/P1 - Description of the Problem#^MutualEx\|mutual exclusion]]*

Each thread initialises a shared `lock=0`. Only one thread can get the lock and execute its critical section.
![Pasted image 20250122010411.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250122010411.png)
##### Compare-And-Swap Instruction
![Pasted image 20250122010655.png|500](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250122010655.png)
This is a definition of the instruction $\rightarrow$ Implemented in hardware
- These steps happen **atomically—compare-and-swap** cannot be interrupted
- In a multiprocessor, **compare-and-swap** also happens sequentially in arbitrary order
	- Set `val` to `new` only if the value is what we expected

**Compare-and-swap** can be used to implement *[[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W8 - Process Synchronisation/P1 - Description of the Problem#^MutualEx\|mutual exclusion]]*

Each thread initialises a shared `lock=0`. Only one thread can swap the lock to 1 and execute its critical section.
![Pasted image 20250122011020.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250122011020.png)

>[!warning] Test-and-set and Compare-and-swap
>The solutions presented above do not meet the **[[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W8 - Process Synchronisation/P1 - Description of the Problem#^BoundedWait\|bounded waiting]] requirement**:
>- a thread may be stuck at the atomic instructions, waiting, while other threads keep getting the lock

##### Atomic Variables
The **compare-and-swap** instruction is often used to build other tools for synchronisation

**Atomic variables** provide atomic operations on basic data types; only one thread at a time can modify them

They can be used to avoid **race conditions** on single shared variables, when multiple threads are updating them

Most systems that support **atomic variables** also provide *atomic data types* and operations on them

>[!info] Atomic Variables
>These variables are useful in operating systems for limited uses, such as updating single-variable features like counters

