---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w7-scheduling/p6-scheduling-with-deadlines-real-time-processing/"}
---


### Real-Time CPU Scheduling
Real-time systems can be categorised into two types:
1. Soft real-time:
	- Guarantees preference for critical processes
2. Head real-time:
	- Guarantees completion by a deadline
The two types of latencies that affect performance:
1. Interrupt latency:
	- The time from arrival to the interrupt service routine
![Pasted image 20250121200913.png|300](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250121200913.png)
2. Dispatch latency:
	- The time for the dispatcher to stop the current process and start another
![Pasted image 20250121200945.png|300](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250121200945.png)

>[!abstract] Hard real-time systems
>Various latencies should be bounded to meet the strict requirements of these systems

### Priority-Based Scheduling
>[!tip] Real-time systems
>It is essential to have a priority-based preemptive scheduling for real-time systems. Usually real-time processes have the highest priority

Priority-based preemptive scheduling gives us soft real-time functionality

Additional scheduling features are required for hard real-time
Some definitions:
- Processes are periodic—They require the CPU at constant intervals
- Processing time $t$, deadline $d$, period $p$. Where $0\leq t\leq d\leq p$

>[!important] Admission Control
>Schedulers take advantage of these details and assign priorities based on the deadlines and periods. The **Admission control** algorithm may reject the request as impossible to service by the required deadline

### Rate-Monotonic Scheduling
Upon entering the system, each periodic task is assigned a priority of $\frac{1}{p}$
- i.e. prioritise processes that require the CPU more often (less period $=$ higher priority)
>[!warning] 
>This can cause problems with some systems as processes with higher periods can be starved so till they miss their deedline:
>![Pasted image 20250121204326.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250121204326.png)
>![Pasted image 20250121204342.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250121204342.png)
>Here, $P_{2}$ fails to meet its deadline of $80$
>
### Earliest-Deadline-First Scheduling
Order by the earliest (closest) deadline—allows for changing of priorities
![Pasted image 20250121204533.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250121204533.png)
>[!info] EDF Scheduling
>No requirement of the period, just the deadline, therefore processes do **not** need to be periodic as with [[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W7 - Scheduling/P6 - Scheduling with Deadlines; Real-Time Processing#Rate-Monotonic Scheduling\|#Rate-Monotonic Scheduling]]
