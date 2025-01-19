---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w3-processes/p3-process-manipulation/"}
---


### Operations on Processes
#### Creation
Processes may create several new processes during execution!

The ‘creating’ process is called a **parent process** and the new processes are called **children processes**
New processes can in turn create more—this forms a **tree of processes**

The **Process Identifier (pid)** is usually used to identify each process
![Pasted image 20250119211216.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119211216.png)
$$\boxed{\begin{array}{c}\text{systemd created on boot; it starts the processes for various services}\end{array}}$$
There are two options for providing resources to a child process:
- Obtain directly from the OS
- Share a subset of the resources from a parent
$$\boxed{\begin{array}{c}\text{Restricting child processes to a subset of the parent's resources avoids}\\\text{overloading the system through the creation of many child processes.}\end{array}}$$

When a process creates another process, there are two possibilities
- The Parent and Child execute **concurrently** (not necessarily in *parallel*)
- The Parent waits until some or all of its children terminate

The Address space also has two possibilities:
- The Parent and Child have the same program and data (`xv6 fork()`)
- The Child has a new program loaded into it (`xv6 fork()` and then `exec`)

In UNIX, a new process is created by `fork()`:
- The new process has a copy of the address space of the original process
	- Initially they share the same memory, however it is marked as read-only and if either try to modify it the OS creates a copy for them to use instead. (**copy-on-write (COW**)
		- This allows for much more efficient memory management when dealing with large process trees
		- This is **NOT** used in `xv6` but is widely used in UNIX
After the `fork()`, usually `exec()` is called:
1. Process’ memory space is replaced by a new program
2. Load a binary file into memory
3. Destroy the memory image of the program containing the `exec()` system call
4. The parent can then create more children, or wait until the termination of its current ones
![Pasted image 20250119212520.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119212520.png)
#### Termination
The process terminates when it asks the OS to delete it using the `exit()` system call
All the resources: physical and virtual memory, open files, and I/O buffers are reclaimed by the OS

A parent may forcibly terminate its created processes:
- If the child process has exceeded its usage of some allocated resources
- If the jobs that the child is doing is no longer required
- If the parent is exiting and is required to terminate the sub-tree of processes before exiting (**cascading termination**)
>[!abstract] Zombie Processes
>Parents may call `wait()` to wait for their children to terminate. The processes that have terminated but whose parents have not yet called `wait()` are called zombie processes—we have to keep them in the system to return the status to the parent eventually.
>	- However, the memory for the child is reclaimed upon its termination—it just hasn’t returned its exit status yet

