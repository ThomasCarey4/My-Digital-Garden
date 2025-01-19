---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w1-introduction-to-os/p5-single-and-multi-processor-systems/"}
---


### Single-Processor Systems
A single processor containing one CPU with a single processing core.
The **core** is the main piece of hardware within a CPU that executes program instructions and manages register storage locally

**General purpose** or **domain specific**: can run general programs or can run a limited set of operations optimised for some task/s.

A computer system may have one general purpose single-processor CPU and multiple domain-specific processors that accelerate some specific tasks. From the perspective of OS, the system is still a single processor.
### Multi-Processor Systems
Two or more processors, each with a single-core CPU
The main goal is to increase **throughput**—how much work can we do in a certain amount of time
Ideally $N$ processors should result in an $N$ times speed up. In reality it is less: there is some overhead in managing multiple processors that cooperate on some task. This overhead does not exist when only processor is executing.

**Symmetric Multiprocessing**
![Pasted image 20250118191558.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250118191558.png)
Nowadays we use **multi-core** systems
![Pasted image 20250118191735.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250118191735.png)
#### Main Terms
- **CPU** — The hardware that executes instructions
- **Processor** — A physical chip that contains one or more CPUs
- **Core** — The basic computation unit of the CPU
- **Multi-core** — Including multiple computing cores on the same CPU
- **Multi-processor** — Including multiple processors
