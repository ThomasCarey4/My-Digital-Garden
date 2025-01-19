---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w3-processes/p2-scheduling-of-processes/"}
---

### Process State Transitions
$\boxed{\begin{array}{c}\text{Processes change }\textbf{states}\text{ during execution!}\end{array}}$
- **New**: The process has been created
- **Running**: The CPU is reading the process’ instructions
- **Waiting**: Waiting for an event (e.g. I/O completion)
- **Ready**
- **Terminated**
$$\boxed{\begin{array}{c}\text{Note that only one program can be }\textbf{running}\text{ on a }\textit{core}\text{. Others may be }\\ \textbf{ready}\text{ or }\textbf{waiting}\text{.}\end{array}}$$
![Pasted image 20250119202800.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119202800.png)
### Process Control Block (PCB)
$\boxed{\begin{array}{l}\text{The OS keeps track of processes using a }\textbf{process control block (PCB)}\end{array}}$
The **PCB** tracks a process’:
- **State**
- **Program Counter (PC)**
- **CPU Registers**: Along with the PC, these have to be saved when the process is interrupted
- **CPU-Scheduling Information**: Priority and other scheduling parameters
- **Memory-Management Information**: The location of various memories assigned to the process
- **Accounting Information**: Resource utilisation statistics
- **I/O Status Information**: I/O devices allocated to the process, open files, …
![Pasted image 20250119203754.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119203754.png)
#### Linux Example
![Pasted image 20250119203908.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119203908.png)
### Processes or Threads?
>[!abstract] Multi-threading
>Nowadays Operating Systems extend processes to be able to perform multiple tasks at once—for example, two cores executing at different locations in the binary of a process. The PCB and other parts of the OS have to be expanded.

### Process Scheduling
The objective of [[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W1 - Introduction to OS/P6 - Key Concepts for OS#Multi-Programming\|multi-programming]] is to maximise CPU utilisation

**Time-sharing** (or [[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W1 - Introduction to OS/P6 - Key Concepts for OS#Multitasking\|multitasking]]) adds another requirement—the switching between processes should be frequent enough for users to interact with the running programs
>[!abstract] Process Scheduler
>An integral art of Operating Systems which meets the constraints posed by time-sharing and multi-tasking by selecting a process to run from a set of available processes

>[!abstract] Multiprocessing
>Each CPU core can run one process at a time: $N$ CPUs can run $N$ processes. If more processes than cores are created, some will have to *wait*. The **Degree of Multiprogramming** defines the number of processes currently in memory

There are two types of processes:
- **I/O Bound**: Spend most of their time *waiting* for memory
- **CPU Bound**: Spend most of their time in execution
The types of processes going through the system will affect the objectives of multiprogramming and time-sharing
#### Queues
Processes enter the system and put into a **ready queue**
The queue is usually a singly linked list, where each PCB links to the next
There may be other queues, for example: a **wait queue** for processes waiting for I/O
#### CPU Scheduler
$$\boxed{\begin{array}{c}\text{Role of a scheduler: from a set of }\textbf{ready}\text{ select one and run on the CPU}\end{array}}$$
- I/O bound processes may execute for a few milliseconds before wait for I/O
- CPU bound processes may require the CPU for extended durations, but the scheduler is unlikely to grant it
The scheduler is typically designed to switch processes very frequently (less than every 100 milliseconds)
>[!abstract] Memory Swapping
>This technique may decide to move a process from memory to disk, reducing the **degree of multiprogramming** and thus reducing active contention for the CPU. Later, the process can be returned to memory and continued where it left off (state save/restore required)

#### Context Switching
**Interrupts** cause the CPU to pause the current task and do some **kernel ** routine
- The CPU needs to save the current **context** of a process and later restore it to continue running it
- The context is represented in the [[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W3 - Processes/P2 - Scheduling of Processes#Process Control Block (PCB)\|PCB]] of the process
>[!abstract] Context Switch
>Perform a **state save** of the current process and a **state restore** of a different process

$$\boxed{\begin{array}{c}\text{Context switching is pure overhead as the CPU}\\ \text{does not execute any process instructions}\end{array}}$$
Typical speed: several microseconds. Depends on the size of the state needed to save/restore
![Pasted image 20250119210944.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119210944.png)
