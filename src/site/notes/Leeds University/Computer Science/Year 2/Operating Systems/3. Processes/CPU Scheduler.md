---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/3-processes/cpu-scheduler/"}
---


- The scheduler is working frequently
- I/O bound processes may execute for a few milliseconds before waiting for I/O
- CPU-bound processes may require the CPU for extended durations, but the scheduler is unlikely to grant it
- Typically designed to switch processes very frequently (less than every 100 milliseconds)

>[!abstract] Memory Swapping
>The technique may decide to move a process from memory to the disk, reducing the **degree of multi-programming** and thus reducing the active contention for the CPU. Later the process can be returned to memory and continued where it left off (state save/restore required)

###### Context Switching
**Interrupts** cause the CPU to pause the current task and do some **kernel** routine
- The CPU needs to save the current **context** of a process and later restore it for continuing to run it
- Context is represented in the PCB of a process
	- Register contents, state of the process, memory management information

>[!abstract] Context Switch
>Perform a **state save** of the current process and a **state restore** of a different process

>[!tip] 
>The Context Switch is pure overhead as the CPU is not executing any process instructions

Typical speed: several microseconds. Depends on the size of the state needed to save/restore

