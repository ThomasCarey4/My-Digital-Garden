---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w9-memory-mangement/p5-virtual-memory/"}
---


The memory management we discussed so far is stemming from a basic requirement:
**instructions should be in memory for execution**
- Downside: The size of the program is limited to the size of physical memory
- The entire program may not be needed, for example:
	- Code for error conditions; errors rarely occur
	- Large arrays when not all elements are used
	- Generally, features of large programs that are rarely used

>[!question] Store the program in memory only partially?
>Benefits:
>- The Program size is not constrained by the size of physical memory
>- More programs can be run concurrently
>- Less I/O needed when loading/swapping programs

>[!abstract] Virtual Memory
>Provide an extremely large memory space for the programmer’s view: **logical space**. This space is implemented by a combination of smaller **physical memory** space and **large (but slow) disk** space, by moving pages between the disk and the physical space as required

>[!abstract] The programmer’s view
>Virtual memory allows the programmer to not worry about the physical space limitations and concentrate on solving the problem in the virtual space.

![Pasted image 20250122130219.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/W9%20-%20Memory%20Mangement/images/Pasted%20image%2020250122130219.png)
Here you can sees some memory is in physical memory and some is in the store

![Pasted image 20250122130346.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/W9%20-%20Memory%20Mangement/images/Pasted%20image%2020250122130346.png)
No physical memory is used until pages are requested by, for example, `malloc` or dynamic linking

![Pasted image 20250122130428.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/W9%20-%20Memory%20Mangement/images/Pasted%20image%2020250122130428.png)
Each process thinks that the shared memory is in their virtual address space, but the logical addresses are mapped to the same shared pages in the physical memory

### Demand Paging
…
**Pure Demand Paging** — *Never* bring in a page until it is addressed

When replacing a frame, **Zero-fill-on-demand** is used to zero-out the previous data

### Copy-on-write
Used when `fork()` is called to prevent duplicating the entire memory, instead pages will be shared until either process tries to write to them, then they get given their own copy

#TODO !
