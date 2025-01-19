---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w6-threads-and-concurrency/p1-the-concept-of-threads/"}
---


### Introduction
$$\boxed{\begin{array}{c}\texttt{xv6}\text{ only supports single-threaded processes}\end{array}}$$
>[!question] What is a Thread?
>A basic unit of CPU utilisation; it comprises a **thread ID**, a **program counter (PC)**, a **register set**, and a **stack**

- All the threads within a program share: code section, data section, and other resources (e.g. open files)
- A traditional process has only a single thread of control
- Processes with multiple threads can preform more than one task at a time
![Pasted image 20250119222814.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119222814.png)
Examples:
- An application creating photo thumbnails from a collection of images uses a different thread for each image
- A web browser displays images or text in one thread and retrieves network data in another
- A word processor has a thread to display UI, a thread to respond to keystrokes, and a thread for spellchecking
>[!abstract] Multicore Systems and Threads
>Applications can be designed for threads to run in parallel on multicore systems

>[!example] Multithreading  in a Web Server
>In some situations, applications may be required to perform several similar tasks
>For example, a web server accepts client requests for web pages, images, sound, etc
>
>Several users may request access at the same time!
>**Running a single thread, the web server would hold other users, potentially for prolonged periods**
>
>One approach: A tree of processes, with the root being the server and children being user requests—time consuming process creation and significant resource use
>
>Since similar tasks are performed on requests, **multithreading is a more efficient solution**
>
>![Pasted image 20250119223429.png|400](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119223429.png)

Other motivating aspects:
- Most OS kernels are multithreaded; for example, during Linux boot time, threads are created for managing devices, memory management, and/or interrupt handling
- Various applications that parallelise well can take advantage of multithreading: sorting, tree algorithms, graph algorithms
- Data mining, artificial intelligence: people aim to design algorithms to **exploit multicore architectures**
- Sometimes problems are **embarrassingly parallel**, without data dependencies, such as adding two vectors together. These problems can be easily solved across many cores
### Benefits
- **Responsiveness**: If one part of an application blocks, other threads can continue working
- **Resource Sharing**: Threads can share memory resources of a process to which they belong
- **Economy**: Allocating resources when creating processes is costly; context switch is also costly. Threads are cheaper in both aspects
	- As they share so much between each other there is less to “switch”
- **Scalability**: Multi-threaded processes can exploit multiple cores, whereas a single-threaded process can only run on one core
