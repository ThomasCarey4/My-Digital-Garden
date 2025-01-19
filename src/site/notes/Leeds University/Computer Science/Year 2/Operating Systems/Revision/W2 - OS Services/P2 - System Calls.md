---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w2-os-services/p2-system-calls/"}
---


**System Calls**: A well-defined interface to the services of an operating system, used by programmers and users

Usually written in C or C++, but assembly can also be used

Consider an example task of reading a file and writing its contents to another file. As a UNIX command it may look like this:
$$\boxed{\text{cp in.txt out.txt}}$$
In this simple tasks, may OS services are employed:
1. Entering the command, or moving a mouse to select files, causes a sequence of I/O system calls
2. Then, files need to be opened: another set of system calls
3. Errors need to be detected: input file not existent, output file already exists…
	1. Can ask the user if they want to replace the output file—requires another set of system calls
4. When both files are open, we loop by reading bytes from one to another (system calls)
5. Each read must return possible error conditions: end-of-file (EOF), hardware failure tor ead, …
6. Once done, the files should be closed (system calls)

### Application Programming Interface
Most programmers will not see this level of complexity of numerous OS services being in use

APIs hide this away behind a set of standard functions which are made available to programmers, for performing common tasks when developing applications

Input and output parameters are specified for each API function

Common APIs:
- Windows API
- POSIX API (UNIX, Linux, macOS)
- Java API (Applications based on the Java Virtual Machine (JVM))
$$\boxed{\text{APIs provide code portability and eases the task of using OS services!}}$$
![Pasted image 20250118220535.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250118220535.png)
>[!abstract] System Call Interface
>This is an abstraction that allows programmers to not think about the details of system calls being used in API functions. The user only needs to obey the API and understand the effects of calling it

### System Calls
#### Parameter Passing
System calls requires various information, for example, files, devices, addresses in memory, lengths of byte streams, …

Three methods to pass parameters to the OS:
1. Store them in the registers directly
2. To store them in a table and the address to it is passed through a register
3. To push them to a stack by a program and popped off the stack by the OS
#### Types
We can roughly group system calls into six categories:
1. [[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W2 - OS Services/P2 - System Calls#Process Control\|#Process Control]]
2. [[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W2 - OS Services/P2 - System Calls#File Management\|#File Management]]
3. [[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W2 - OS Services/P2 - System Calls#Device Management\|#Device Management]]
4. [[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W2 - OS Services/P2 - System Calls#Information Maintenance\|#Information Maintenance]]
5. [[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W2 - OS Services/P2 - System Calls#Communications\|#Communications]]
6. [[Leeds University/Computer Science/Year 2/Operating Systems/Revision/W2 - OS Services/P2 - System Calls#Protection\|#Protection]]
##### Process Control
- The running program needs to halt its execution
	- If the termination is abnormal, some log files are usually generated
	- A **debugger** may use those logs to aid the programmer in fixing problems
	- **Bugs** are usually discovered this way in the code
- When a process is running, it may want to **load** and **execute** other programs
- Create, terminate, duplicate, wait for processes
- Get information about a process
- Where data is shared among processes, **locking** is provided to assure no clashes ensue
##### File Management
Common system calls that deal with files:
- **Create** and **delete** files
- **Open** files for reading and writing
- Similar operations are required for directories
- Determine and set attributes: file name, type, protection codes, …
##### Device Management
Processes may need resources to execute: main memory (RAM), disk drives, access to files, …

Resources available can be granted, but usually processes will have to wait for them.

We can think of resources as **devices**: physical or virtual

The OS provides system calls for interacting with these:
- Request and release a device
	- Similar to open and close system calls for files
- Once we have the device allocated to use, we can read and write
- File handling and general device is so similar that *UNIX merge the two*!
##### Information Maintenance
There are system calls for transferring information between the OS and user programs:
- Time and date calls
- Version of OS
- Amount of free memory or disk space
- Memory **dump**s
- Other debugging info usually provided: single step, runtime profiling, program counter recording, various information about processes, …
##### Communications
Processes need to communicate, and there are two main methods: **message-passing model** and **shared-memory model**
>[!info] Message-Passing Process Communication Model
>Processes exchange messages with one another to transfer information. Before communication takes place, the connection must be opened. The computers’ **Hostname** and **Process Name** are used to identify the possible remote parties for communication. System calls to establish or abort communications are available. Other system calls to receive and send messages are also available.

>[!info] Shared-Memory Model
>Processes use system calls to create and gain access to regions of memory owned by other processes. Normally, the OS prevents processes from accessing memory allocated to other processes. In the shared-memory model, processes have to agree to remove the obstruction

##### Protection
The OS should provide services for protecting computer system resources
Traditionally this was to protect one user from another on an instance of some OS
With the Internet, all systems started to get concerned about protection
System calls include setting permissions of files and disks
- Allow/deny access for particular users (or groups)
### System Services
>[!abstract] OS System Services
>This is separate from **System Calls** within the OS. **System Services** are sitting between the OS and the Application Programs. They can also be called **System Utilities**

![Pasted image 20250118165159.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250118165159.png)

Some system services are interfaces to system calls, but some are more complex, For Example:
- File Management: Create, Delete, Copy, Rename, Print, List files/directories
- File Modification: Editing a file
- Status Information: Time, Date, Memory space, Debugging information
- Programming Language Support: Compilers, Assemblers, Interpreters, Debuggers
- Program loading and execution
**Application programs** supplied with OS are usually higher level tools that utilise many **system services**: browsers, word processors and text formatters, spreadsheets
$$\boxed{\begin{array}{c}
\text{Most users view the OS through application programs and}\\\text{system services, not system calls}\end{array}}$$
