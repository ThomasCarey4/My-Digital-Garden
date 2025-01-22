---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w7-scheduling/p3-scheduling-algorithms/"}
---


### First-Come, First-Served (FCFS) Scheduling
![Pasted image 20250120212427.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120212427.png)
If a process arrive in a sequence we have the following schedule:
![Pasted image 20250120212915.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120212915.png)
Obviously, this is crap and a better sequence would be if (assuming $P_{2}$ and $P_{3}$ don’t depend on $P_{1}$):
![Pasted image 20250120212934.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120212934.png)
>[!warning] Issue with FCFS
>**Convoy effect**—short jobs can be held waiting by long jobs.

Note that **FCFS is nonpreemptive** (**Not** able to be interrupted)
### Shortest-Job-First (SJF)
1. Append each process with the length of the *next* CPU burst
2. Schedule the jobs with the shortest time
3. **SJF** is optimal, but it is difficult to know future CPU burst lengths
4. Ties broken with FCFS scheduling (i.e. same burst time)

- Better name: **shortest-next-CPU-burst**
- **SJF** is **nonpreemptive**!
![Pasted image 20250120213426.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120213426.png)
#### Predicting the Lengths of Future CPU Bursts
>[!tip] Make an assumption
>Next CPU burst likely similar to the past bursts

- $t_{n}$—The actual length of the CPU burst $n$
- $\mathcal{T}_{n+1}$—The predicted value of the next burst
- $0\leq\alpha\leq1$
- $\mathcal{T}_{n+1}=\alpha t_{n}+(1-\alpha)\mathcal{T}_{n}$
- We can tune this model through $\alpha$ (usually set to $0.5$)
![Pasted image 20250120213841.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120213841.png)
>[!abstract] Exponential average of past CPU bursts
>We can model $\mathcal{T}$ as a recurrence relation, as each term is based on the previous terms (with each successive term having a lower weighting, with the initial guess having the lowest)

#### Shortest-Remaining-Time-First
If we allow SJF to be preemptive, it can interrupt a currently running process if it would run longer than some new process

Consider:
![Pasted image 20250120215711.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120215711.png)
### Priority Scheduling
>[!tip] Priority Scheduling
>Shortest-job-first is a specific case of general scheduler that decides by priorities

1. A priority (integer) associated with each process
2. The CPU allocated to the process of highest priority

- **Starvation**—Low priority processes may not execute
- **Ageing**—Increase the priority proportional to waiting time
- **Internal Priorities**—Time limits, memory requirements, ratio of average I/O burst
- **External Priorities**—The importance of the process, type and amount of  funds being paid for the CPUs, who is asking to the run the process, and other

>[!info] Preemptive Priority Scheduling
>Priorities may change while a process is running

### Round Robin (RR) Scheduling

- **Time Quantum** ($q$) is defined
- The CPU scheduler assigns the CPU to each process for an interval of up to $1$ quantum
- The queue treated as First-In-First-Out
- Interrupts every quantum to schedule next process
- **RR is therefore *preemptive***
- No process is allocated for more than $q$ in a row (unless there is only one)

- If there are $n$ processes waiting, each process is guaranteed to get $1/n$ of CPUs time in chunks of time quantum $q$
- Each process must wait no longer than $(n-1)\times q$ time units until its next turn to run

Take $q=4$
![Pasted image 20250120222026.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120222026.png)
- Small quantum—too many interrupts will reduce performance
- Big quantum—scheduler similar to FCFS
	- Most processes finish before their quantum is up
- Need a balance (according to OSC, usually $q=10$ to $100$ ms)
- Context switch around $10$ microseconds (small fraction of $q$)

- **Turnaround time** depends on the size of the quantum
- However, it does not necessarily improve with the size of $q$

>[!important] Rule of Thumb
>$80\%$ of CPU bursts should be shorter than $q$

