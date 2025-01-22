---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w8-process-synchronisation/p5-other-problems-in-synchronisation/"}
---


### Liveness
Using synchronisation tools to coordinate processes introduces a possibility for processes to *wait indefinitely*

**Liveness**: A system *must* ensure that processes can make progress
- A process waiting indefinitely means our operating system produces a *liveness failure*
$$\boxed{\begin{array}{c}\text{Providing semaphores and mutex locks opens up a possibility for liveness failure}\end{array}}$$
#### Deadlock
$\large S=Q=1$
![Pasted image 20250122015843.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250122015843.png)
>[!error] Deadlock
>Every process in the set is waiting for an event that can only be caused by another process in the same set. Since the other process is also waiting, no progress will be made and the set is **deadlocked**
>

#### Priority Inversion
Consider a scenario where a higher-priority process needs to read/modify kernel data held by a mutex lock by a lower-priority process
- The high priority process waits for the lower-priority one:
		- a scheduling problem!

>[!example] Priority Inversion Example
>Take processes $A,B,C$ with priorities $A>B>C$. Imagine that process $A$ wants a semaphore $S$, which is held by $C$. Then image that process $B$ preempts $C$ and gets scheduled since it is of higher priority. $B$ has affected how long a higher-priority process $A$ must wait for the semaphore.
>
>>[!tip] 
>>Avoid this by implementing a **priority-inheritance protocol**!
>>- If a process accesses a resource needed by a higher-priority process, it inherits that higher-priority
>>- The priority is reduced back to the original priority when the resource is released

