---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w6-threads-and-concurrency/p4-threading-issues/"}
---


### `fork()` and `exec()` calls
We have seen `fork()` and `exec()` in a small UNIX system:
- Create a child, and
- Load and execute a binary

This becomes difficult in a multithreaded environment:
- Does `fork()` duplicate the thread or the whose set of threads within a process?

Different `fork()` functions may be provided to achieve either

The `exec()` call typically works as usual: The entire process is replaced by the specified program
$$\boxed{\begin{array}{c}\text{Which }\texttt{fork()}\text{ to use depends on the application}\end{array}}$$
### Signal Handling
**Signalling** in UNIX is used to inform processes of events
1. The occurrence of some event generates a signal
2. The signal is delivered to a process
3. The process handles the signal
Example events:
- Division by zero
- Illegal memory access
- CTRL-C key combination
$$\boxed{\begin{array}{c}\text{Which thread should a signal be delivered to?}\end{array}}$$
Various methods exist, for example:
- Deliver to all threads
- Assign one thread to deal with signals
	- If that thread receives a SIGKILL, it just dies and the OS notices and kills the rest of the threads + process
On UNIX:
$$\texttt{kill(pid\_{t} pid, int signal)}$$
Threads will either accept or block the signal. The first thread to accept receives it
>[!tip] 
>Yeah `kill()` is **not** just for killing programs (bloody stupid if you ask me), it’s used for sending signals—which *could* be a kill or terminate signal…

### Thread Cancellation
We may want to terminate threads before they complete, called **target threads**

For example, threads looking through a database for something can stop when one finds the item.

Problems can occur if the target thread is updating shared data while being cancelled
`pThreads` for example allows threads to disable cancellation for some time
