---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w7-scheduling/p5-remarks-on-multi-processor-scheduling/"}
---


### Multi-Processor Scheduling
Traditionally the term **multi-processor** referred to systems with multiple *physical* cores. Now we use it to describe systems with either several physical or virtual cores/threads

One approach to scheduling is to have one master processor handling scheduling (**asymmetric multiprocessing**).
The Master then becomes a bottleneck :(

Another is **Symmetric multiprocessing (SMP)**—each processor handles its own scheduling. This is the most common (Windows, Linux, macOS, Android, iOS, …)
#### SMP
There are two approaches to SMP
1. Common ready queue—each processor takes processes/threads from that queue (potential clashes)
2. Each processor has its own queue
![Pasted image 20250120230927.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120230927.png)
### Multicore Processors
A relatively recent trend is trend is to place multiple cores on a chip (**multicore**)
- Speed and energy efficiency 
- **Memory stall**—cores spend a significant amount of time waiting for memory (since nowadays cores are *much* faster than memory)
- **Multithreading**—hardware assisted multiple threads per core
	- When one thread is in a memory stall, work on another
	- The OS treats different hardware threads as separate CPUs
![Pasted image 20250120231222.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120231222.png)
### Load Balancing
With SMP we need to utilise all CPUs efficiently
- Load balancing attempts to even the distribution of tasks
- Only necessary on systems with separate queues for each CPU
- **Push migration**—A task checks the load on each CPU and balances the threads
- **Pull migration**—An idle processor pulls waiting tasks from busy processors
#### Processor Affinity
When a thread runs on a core, the cache is “warmed up” for that thread
- We say that task has affinity for the processor it’s running on
- When a task is moved, say due to load balancing, there is a big overhead in terms of cache
	- Invaliding and repopulating cache is expensive
- **Soft affinity**—The OS will attempt to keep the process on the same core, but load balancing will move it
- **Hard affinity**—Processes specify a list of processors on which to run
- Usually both methods are available :)

>[!abstract] Implications on Scheduling
>Load balancing and processor affinity both may have implications on scheduling

