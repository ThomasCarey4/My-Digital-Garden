---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w3-processes/p4-communicating-processes/"}
---


### Interprocess Communication
A process on the system can either be: 
- **Independent**:
	- Not sharing any data while executing
- **Cooperating**
	- If it can affect or be affected by other processes

Process cooperation is useful in a few different scenarios:
- **Information Sharing**: For example, copy-paste between programs
- **Computation Speedup**: Split big tasks into multiple subtasks
- **Modularity**: The system may be designed to have separate processes or threads working cooperatively to achieve some function
$$\boxed{\begin{array}{c}\text{When processes cooperate, they require }\\ \textbf{Interprocess Communication (IPC)}\end{array}}$$
There are two fundamental concepts:
- **Shared-memory model**: They agree on a region of memory to share among cooperating processes. They read/write there to exchange info
- **Message-passing model**: They use a message-passing protocol to send and receive information
	- Likes `.fifo` pipes!
	- or `|` pipes!
Both are implemented in the Operating System

The message-passing model is useful when no conflict resolution is desired.
However, it is slower, since each read/write requires kernel operations

With the shared-memory model, conflicts and race conditions may appear (two processes write)

Message-passing is required to communicate between different systems that do not share memory
#### Pipes
**Pipes** were one of the earliest UNIX mechanisms for interprocess communication
##### Ordinary Pipes (Unnamed)
- **Producer-Consumer** model:
	- The producer writes to the **write end** of the pipe, while the consumer reads from the **read end**
- **Unidirectional**:
	- We need two pipes for communication back to the producer
- In UNIX this is constructed using `pipe(int p[])` where `p[0` is the read end of the pipe and `p[1]` is the write end
	- `p[0]` and `p[1]` are special types of *files* in UNIX, therefore `fork()` in the parent will make the child inherit these
##### Named Pipes
**Ordinary pipes** provide a simple mechanism for processes to communicate, but they only exist until processes exist and communicate. When they terminate, the pipe disappears

**Named pipes** (FIFOs) in UNIX provide extra functionality:
- Bidirectional communication
	- Can only communicate one direction at a time (think a one-lane road)
- No parent-child relationship needed
- Several processes can use the pipe for communication
- The pipe remains active after the communicating processes terminate
