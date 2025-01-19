---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w3-processes/p1-introduction-to-processes/"}
---


### What is a Process?
Early computers only executed one program at a time
	- That program had complete control over all resources
Today: multiple programs are stored in memory, all executed through[[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W1 - Introduction to OS/P6 - Key Concepts for OS#Multitasking\|multitasking]]
	- This evolution required the compartmentalisation of various programs
>[!abstract] Process
>A **Process** is a program in execution. One program invoked multiple times results in multiple *processes*.

#### A Concept of Processes
Early computers were **batch systems**: executing **jobs** submitted by users
	- Minimum interaction
This was followed by **time-shared** systems: **user programs** or **tasks**
	- Potentially interacting
Even one user can run several tasks: browser, email, editor, etc
>[!abstract] Jobs
>Calling running programs **jobs** has historical significance, as most of the OS concepts were developed around job processing. You may see the term used to this day, but **process** is a modern replacement


The status of the current activity of some process is represented by
- The current value of the **program counter**: where are we in the execution of the binary?
- The contents of he CPU **registers**: what data are we working with/on?
##### Memory Layout
Each process has its own memory layout:
- **Text section:** Executable code
- **Data**: Global variables
- **Heap section**: Memory that grows and shrinks dynamically during execution
- **Stack**: A structure for temporary values (function parameters, return addresses, and local variables)

$\boxed{\begin{array}{l}\text{The Text and Data sections are fixed size.}\\ \text{The Heap and Stack change size}.\end{array}}$
![Pasted image 20250119201431.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119201431.png)

##### Stack
The **Stack** contains a potentially small amount of data which is **pushed** and **popped** using specific CPU instructions
For example, when a function is called, input arguments, local variables, and the return address are **pushed** on the stack.
Upon completing the function, data is **popped** from the stack: The last one is *usually* the return address to get back the caller

##### Heap
The **Heap** can be grown dynamically
	- In C `malloc` and `free` do that for us
Usually the **heap** and **stack** grow toward each other—the overlap watched by the OS
In xv6, process memory is slightly different:
![Pasted image 20250119201859.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119201859.png)
