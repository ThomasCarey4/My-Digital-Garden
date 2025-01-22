---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w8-process-synchronisation/p2-software-solutions-to-process-synchronisation/"}
---


### Race Conditions in the Kernel
#### File Opening/Closing
Consider a *kernel data structure* that maintains **a list of open files** in the system
- It must be modified when a new file is opened/closed
- If two processes open/close files simultaneously, there may be a **race condition** on this data structure
#### Getting PIDs
![Pasted image 20250121211213.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250121211213.png)
### The Critical-Section Problem
In a single-core environment, the critical-section problem can be solved by simply disabling interrupts during the execution of critical code as there is nothing else running.
#### In the Kernel
There are two approaches used in kernels:
1. Preemptive Kernels
2. Nonpreemptive Kernels
		- Only works on single-core?

The latter does not allow processes to be interrupted while they are in kernel mode. Safe from race conditions on kernel data structures

#### A Basic Software Solution
**Peterson’s Solution**
![Pasted image 20250121212229.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250121212229.png)
>[!warning] 
>This **does not** work on modern architectures due to **instruction reordering**.
>If you reorder the first two instructions of while loop, the two processes can get confused and think the other is *not* ready, therefore allowing itself to go even when it’s not their turn.
>![Pasted image 20250121220409.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250121220409.png)

