---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w7-scheduling/p4-optimisations-of-process-scheduling/"}
---


### Multilevel Queue Scheduling
With the previous algorithms, it takes $O(n)$ to search the queue

Other methods:
- Assign processes to different queues, by priority
- Assign queues by process types:
	- Queue for **background processes** (hidden)
	- Queue for **foreground processes** (interactive)

Each queue can have different scheduling algorithms, depending on their needs
Scheduling may be required among queues: 
- Commonly fixed-priority preemptive scheduling
		- i.e. each queue has a fixed designated priority

Example queues in decreasing priority levels:
1. Real-time processes
2. System processes
3. Interactive processes
4. Batch processes

> [!info] Multilevel Priority Queue
> No process in a lower priority queue runs while there are processes waiting in the higher priority queues. High priority queues preempt lower priority ones

>[!tip] Time Slicing
>Another possibility is to allocate time among queues.
>For example:
>- $80\%$ to the foreground queue
>- $20\%$ to the background queue

### Multilevel *Feedback* Queue Scheduling
>[!tldr] Dynamic Queueing
>Instead of fixing processes to queues, allow them to move

Multilevel feedback queue is defined by:
- The number of queues
- A scheduling algorithm, for each queue
- A method to upgrade a process to a higher priority queue
- A method to downgrade a process
- A method to determine which queue to assign a process to at the start

>[!tip] Multilevel Feedback Queue
>The most general CPU scheduling algorithm due to its many parameters in the definition

>[!example] 
>Imagine three queues:
>1. $Q_{0}$—RR with $q=8$ ms
>2. $Q_{1}$—RR with $q=16$ ms
>3. $Q_{2}$—FCFS
>   
>   Scheduling:
>   1. A new job enters $Q_{0}$ and gets $0$ ms
>   2. Not finished in $8$ ms? move to $Q_{1}$
>   3. Not finished in $Q_{1}$ in another $16$ ms? move to $Q_{2}$
>   4. Scheduled in FCFS in $Q_{2}$ when queue $0$ and $1$ are empty
>
>>[!tip] Starvation in $Q_{2}$
>>To prevent starvation we may move old processes to $Q_{0}$ or $Q_{1}$

