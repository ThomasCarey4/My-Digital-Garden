---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w1/p6-key-concepts-for-os/"}
---


### OS Operations
As noted earlier, a **bootstrap program** is a key component that starts a computer:
- Stored in nonvolatile memory
- Initialises the CPU registers, device controllers and memory contents
- Loads and starts executing the OS: Locate the **kernel** and load it into the main memory

One the kernel is loaded, it can start providing services to the system and its users.

**System daemons** also run “always”, alongside the kernel, and provide various system services

Once the kernel and daemons are running, the OS is waiting for I/O device requests and other tasks to do. It can sit quietly if nothing is happening

###### Back to Interrupts
- **Hardware Interrupts**: We looked at these. I/O interrupts and other devices
- **Trap Interrupts**: Software-generated interrupts: For example, division by zero or invalid memory address being accessed
### Multi-Programming
A single program cannot keep the CPU or I/O devices bust at all times—the ability to run multiple programs and change between them is **multi programming**
It increases CPU utilisation by swapping which program in execution (a **process**) gets the CPU time
When one process stops executing and starts waiting for I/O to finish, the CPU is allocated to another process that is ready to run
#### Memory Layout
![Pasted image 20250118194643.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250118194643.png)
### Multi-Tasking
Similar to multi-programming, but the switches between processes are very frequent to provide users with a fast **response time**
>[!abstract] Processes
>Having multiple running programs and/or processes, requires some form of memory management. We also need a set of rules for deciding which process gets run (**scheduling**). Processes should also not interfere with other processes.

### User and Kernel Modes of Operation
>[!tldr] Main Idea
>An Incorrect or malicious program should not be able to break the OS, execute code that belongs to OS services, or take over the hardware resources

To avoid these problems, the OS can execute in **user mode** and in **kernel mode (also known as system/supervisor/privileged mode)**

OS services and the kernel are executed in the system mode, while user programs are in user mode. Once a program requests some important resources, it can go into the kernel mode for some specific tasks, **system calls**

![Pasted image 20250118195622.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250118195622.png)
At system boot time, the hardware starts in kernel mode.
Also, on interrupts, the hardware switches to kernel mode
In general, whenever the OS gains control, we are in kernel mode
### Timer: Periodic Interrupts from the OS
For the OS to maintain control over the CPU we need protection against user programs getting stuck in an infinite loop or similar

A **Timer** is set to interrupt the CPU after a specific period
The period can be fixed or variable

The OS sets up the timer before transferring control to the user programs. When the timer interrupt occurs, the OS  takes control and can decide whether to abort the program or let it run longer

Instructions that set up the timer are **privileged instructions**—hardware operations that can only be executed in kernel mode
### Process Management
>[!abstract] What is a process
>A program is compiled and stored in the main memory, as a set of instructions. When the CPU is going through those instructions and executing them one by one, the program takes a form of a **running process**. The concept of processes is fundamental to OS resource management

>[!example] Examples of Processes
>A compiler that is compiling some code; A word processor that has a document open; A social media app open a smartphone


- Processes need resources: CPU, memory, I/O, files, initialisation data
- A program is not a process—it’s a **passive entity**
- Processes instead are **active entities**
- A **single-threaded process** has one **program counter** specifying the next instruction to execute
- Sequential execution: CPU executes instructions one at a time, until the process terminates
- Two processes can be associated to the same program, but are considered separate entities, separate execution sequences
- **Multi-threaded processes** have multiple **program counters**
- Typically many processes exist, some belong to the OS executing in kernel mode, some to the user, executing in user mode:
	- The OS multiplexes between these processes on single or multi-core CPUs

The OS undertakes the following activities in relation to processes:
- Creating and deleting processes
- Scheduling processes and threads on the CPUs
- Suspending or resuming processes
- Provide **process synchronisation**
- Provide ways for **process communication**
### Memory Management
- **Main memory** is central to the operation of a modern computer system
- Main memory can be very large, holding thousands to billions of bytes, each addressed separately
- CPU and I/O devices can target those bytes (read/write)
- Apart from registers and caches, main memory is the only other memory directly accessible by the CPU
- For the CPU to access other data, such as in various disks, it has to be transferred to the RAM first
	- Data and instructions therefore first travel to the RAM
#### Program Execution
1. Load a program into main memory and let the CPU known the start address
2. As a program executes, the instructions and data are accessed by addressing the main memory
3. When a program terminates, space is freed and a new program may take its place in the main memory
4. Several programs are usually in memory, which creates a need for **memory management**
>[!abstract] OS Memory Management
>The OS must:
>- Keep track of used memory blocks and which process is using them.
>- Allocate/deallocate memory space
>- Decide which processes to move in and out of memory

### Cache Management
>[!abstract] Caching
>**Caching** is a technique used to speed-up access to commonly read/written information—the core idea is to copy blocks of information from slower to faster memory and then access it from that faster memory. This state is temporary and caching is happening very frequently at all levels: hardware, OS and software

When we need a particular piece of data, we first check the cache. If it is found, great!. Otherwise, we copy the data from the RAM to the cache—assume it will be needed again

Cache is smaller than main memory. **Cache replacement policy** is an important consideration is OS and can increase performance significantly!
#### Cache Coherence
>[!abstract] Cache Coherence
>In multi-processor environment, each processor may have a separate cache. If both contain the same memory copied from the RAM, and one of them updates it, what happens to the other?
>Cache coherency is needed to make sure the data is not outdated in one of the copies. In distributed systems the problem is severe: same data in different computers!?

### Security and Protection
- The OS protects hardware and memory resources from what can be considered unauthorised access by processes and users
- **Protection**: The mechanism for controlling access to certain resources defined by the computer system
- **Security**: The defence of the system against internal and external attacks: denial-of-service, worms, viruses, identity theft, theft of service, …
>[!abstract] Operating System Security Measures
>Keep track of user IDs; each user ID has associated resources that they can access; each group ID allow sets of users to be assigned permissions

### Virtualisation
Running another OS within the main OS, run applications on that **guest OS**

**Emulation**: The guest OS is compiled for different hardware, which has to be emulated to run on the hardware we have
**Virtualisation**: The guest OS is compiled for our hardware, and runs **natively**, using that CPUs instruction set. This is faster than emulation, but limited

>[!info] XV6
>XV6 uses the RISC-V architecture, meaning we have to translate (emulate) RISC-V instructions into Intel/AMD to run locally

![Pasted image 20250118211013.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250118211013.png)
I don’t know what the link here means :(
### Kernel Data Structures
- [[Leeds University/Computer Science/Year 2/Algorithms 1/Revision/Data Structures#General Case\|Singly Linked List]]
- Doubly Linked List
	- Similar to the singly linked list however, there is also a link to the previous element in the list
- Circularly Linked List
	- Instead of the last element pointing to NULL, it points pack the first element

A **[[Leeds University/Computer Science/Year 2/Algorithms 1/Revision/Data Structures#Stacks\|stack]]** is a common data structure in OS. Interrupt routines push registers to a stack and pop them back to restore the previous state of the CPU.
#### Trees
**Trees** introduce hierarchy: **parent-child structure** between data points
>[!info] Tree Search Complexity
>Unbalanced trees of $n$ nodes can require up to $n$ comparisons to find the data. Balanced trees can improve this by requiring $\log n$ (height of left and right sub-trees differ by at most 1)

#### Hash Maps
**Hash Maps** can allow a search cost of at most 1
![Pasted image 20250118211648.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250118211648.png)
Ideally, each unique key is mapped to a unique value, which can be used as an index to a table containing the data we want

**Hash collisions** can occur: when different keys map to the same value
