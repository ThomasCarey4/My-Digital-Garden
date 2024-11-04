---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/3-processes/process-scheduling/"}
---


The objective of **multi-programming** is to maximise CPU utilisation

**Time-sharing** (or multitasking) adds another requirement—the switching between processes should be frequent enough for users to interact with the running programs

>[!abstract] Process Scheduler
>The process scheduler is an integral part of every operating system which meets the constraints posed by time-sharing and multi-tasking by selecting a process to run from as set of available processes

>[!abstract] Multiprocessing
>Each CPU core can run one process at a time; $N$ CPUs can run $N$ processes. If more processes than cores are created, some will have to *wait*. **Degree of multi-programming** defines the number of processes currently in memory

