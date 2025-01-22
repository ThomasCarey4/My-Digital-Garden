---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w8-process-synchronisation/p1-description-of-the-problem/"}
---


### Motivation
By now we know that the OS typically consists of **many processes/threads** running either **concurrently** or **in parallel**
- Threads often share data!
- The OS continually updates various data structures to support multithreading
$$\boxed{\begin{array}{c}\text{Multiple threads may want to update shared data at the same time}\end{array}}$$
If access to the shared data is not controlled, we may get corrupted data values
- **Process synchronisation** involved methods to control the access to shared data to avoid such issues
### Race Conditions
A **Race Condition** arises when several processes manipulate data concurrently
- The outcome of execution depends on a particular order

It is usually difficult to predict the order of execution and *it may change on different runs* of a multithreaded application
In our example we many need to make sure that only one thread can manipulate $x$ at any time

- **Race conditions** can arise in OS as different parts manipulate shared resources
- **Race conditions** also arise in multithreaded user applications
- The increasing use of multicore systems makes this an important problem!?!?
	- Applications are being developed to run in parallel on many cores, sharing data among different parts
	- Mechanisms to secure against **race conditions** are an important part of the systems these data
### The Critical-Section Problem
Consider a problem with $n$ processes/threads $P_{0},P_{1},\dots,P_{n-1}$
- Each process has a **critical section** of code
- In that section, *shared data* is being accessed (shared among at least two processes)
- When a process is executing instructions in the **critical section**, no other process can do so
- Each process *must request permission* to enter their critical section
	- The **entry section** implements the request
	- The **exit section** may do some tidying up after the critical section
	- The rest of the code is called the **remainder section**

A solution to to this problem should meet the following:
1. **Mutual exclusion**: Only one $P_{i}$ can be in a critical section
{ #MutualEx}

2. **Progress**: If one process asks to execute its *critical section*, only processes not in their *remainder section* can participate
{ #Progress}

3. **Bounded waiting**: There should be a limit on a number of time other processes can enter their *critical section*, when some other process is waiting. Avoid the problem of process **starvation**
{ #BoundedWait}
