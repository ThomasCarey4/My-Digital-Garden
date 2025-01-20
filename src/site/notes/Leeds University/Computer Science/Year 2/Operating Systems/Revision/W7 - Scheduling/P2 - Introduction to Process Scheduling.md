---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w7-scheduling/p2-introduction-to-process-scheduling/"}
---


### CPU Scheduler
>[!tldr] tldr
>When the CPU becomes idle, the OS finds work (**ready process queue**)

The **CPU Scheduler** selects a process from the ready queue and allocates the CPU to it
The Queue may be ordered in various ways :/
CPU scheduling decisions may take place when a process changes state:
1. Running $\rightarrow$ Waiting,
2. Running $\rightarrow$ Ready,
3. Waiting $\rightarrow$ Ready,
4. Terminates

For $1$ and $4$, scheduling is **nonpreemptive**  (Runs when it wants) while $2$ and $3$ are **preemptive** (Can be ***caused*** by an interrupt)

#### Challenges with Preemptive Scheduling
A few scenarios that cause problems:
- Process $1$ is writing data, is preempted by process $2$” that reads the *same* data
- Process $1$ asks the kernel to do some important changes, process $2$ interrupts while they are being done
>[!abstract] Disabling Interrupts
>Irrespective of the challenges, most modern Operating Systems are fully preemptive when running in kernel mode, but disable interrupts on certain small areas of code

#### Dispatcher
The **Dispatcher** gives control of the CPU to the scheduled process
- **Switching context**
- Switching to **user mode** (kernel tasks in **supervisor mode**)
- Jumping to the proper location in the previously interrupted user program (set by the **Program Counter** register)
>[!abstract] Dispatch Latency
>The time it takes for the dispatcher to stop one process and start another

#### Scheduling Criteria
- **CPU Utilisation**—Reduce the amount of time the CPU is idle
- **Throughput**—The number of processes completed per time unit
- **Turnaround Time**—The amount of time to execute a particular process
- **Waiting Time**—The amount of time a process has been waiting in the *ready* queue
- **Response Time**—The amount of time it takes from when a request was submitted until the first response it produced, not output (for time-sharing environment)
>[!tip] When designing a scheduler
>It is desirable to maximise CPU Utilisation and throughput and to minimise turnaround time, waiting time, and response time