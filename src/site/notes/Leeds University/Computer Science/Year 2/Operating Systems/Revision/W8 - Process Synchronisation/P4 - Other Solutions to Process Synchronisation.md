---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w8-process-synchronisation/p4-other-solutions-to-process-synchronisation/"}
---


Hardware-based solutions are complicated and too low-level for application programmers to access

Higher-level software tools are usually available in operating systems
- **Mutex Locks**
- **Semaphores**
### Mutex Locks
A process must acquire a mutex lock before entering a critical section
- It releases the lock when it exits the critical
![Pasted image 20250122013234.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250122013234.png)

The `acquire()` function acquires the lock:
![Pasted image 20250122013256.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250122013256.png)
The `release()` function releases it:
![Pasted image 20250122013320.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250122013320.png)
$$\boxed{\begin{array}{c}\text{Implementations must assure calls to these are }\textbf{atomic}\end{array}}$$
### Semaphores
>[!warning] Mutex Lock Disadvantages
>Mutex locks require **busy waiting**:
>	- While a process is in its **critical section**, other processes loop continuously trying to acquire the lock, until the process holding it releases it

Another method can provide more sophisticated ways for synchronisation:
- A **semaphore** $S$ is an integer variable
- $S$ is only accessed through atomic operations `wait()` and `signal()`
![Pasted image 20250122013817.png|400](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250122013817.png)
#### Used for Access Control to Resources
We can use semaphores to control access to a limited number of resources
1. Initialise $S$ to the number of resources available
2. Processes that wish to use one of the resources call `wait()`: decrement $S$
3. Processes that release resources call `signal()`: increment $S$
4. When $S=0$ all resources have been taken and processes need to block until some become available
5. Because semaphore modifications are atomic, no two processes can capture the same resource
#### Implementing Semaphores
- When `wait()` is called and the process must wait for the semaphore, it will pause itself (**no busy waiting**)
- The process goes to the *waiting queue* and the scheduler selects another
- The process is restarted when some other process calls `signal()`
- Goes from the *waiting queue* to the *ready queue*
- The scheduler may pick it up for running on the CPU
