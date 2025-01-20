---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w6-threads-and-concurrency/p2-introduction-to-parallel-computation/"}
---


**Multithreaded programming** provides a mechanism for an efficient use of multicore systems
### Concurrency or Parallelism?
$$\boxed{\begin{array}{c}\textbf{Concurrency}\text{ (top) and }\textbf{parallelism}\text{ (bottom) refer to different concepts:}\end{array}}$$
![Pasted image 20250119224803.png|500](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119224803.png)

On a single core, concurrency means **interleaving the execution of threads in time.**

On a multicore system, concurrency mean that some threads can execute simultaneously, which means there is parallelism
$$\boxed{\begin{array}{c}\text{We can have concurrency }\textit{without}\text{ parallelism}\end{array}}$$
>[!info] Historical Perspective
>Before multi-processor/core architectures became prevalent, most systems had a single processor and operating systems were designed to *provide illusion of parallelism* by *rapidly switching processes*

### Key Challenges in Designing Programs
System designers and application programmers are pressured to make better use of multiple cores—this is ongoing
The systems are growing in size, both at large (warehouse computers) and small (laptops, phones) scale
- Operating Systems have to accommodate multicore hardware
- Old single-threaded applications have to be ported
- New algorithms have to be developed from scratch (There’s a whole topic on **parallel algorithms**)

The challenges:
1. **Identifying Tasks**: Examine applications and find workloads that can be divided, ideally into independent tasks
2. **Balance**: Make sure parallel tasks perform similar amounts of work
3. **Data Splitting**: The data accessed and manipulated by parallel tasks has to be divided
4. **Data Dependency**: Do tasks depend on the output data of other tasks?
	- **synchronisation** may be required!
5. **Testing and Debugging**: A program running on $N$ cores has many execution paths, making debugging more difficult than in a single-threaded case

>[!info] Interestingly…
>Many people believe that an entirely new software design approach will be needed in the future. Computer Science educators often talk about teaching software development through increased emphasis on parallel programming

### Types of Parallelism

$$\boxed{\begin{array}{c}\textbf{Data Parallelism}\text{ (top) and }\textbf{Task Parallelism}\text{ (bottom)}\end{array}}$$
![Pasted image 20250119225824.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119225824.png)

**Data Parallelism**: Distribute data across $N$ cores, each to receive a *subset* of the whole data
>[!example] 
>Sum a vector of size $K$. Each core gets an equal portion of data to sum

**Task Parallelism**: Distribute different tasks (operations) across multiple cores. Each task may require part or the whole of the input data
$$\boxed{\begin{array}{c}\text{In practice you may likely see a hybrid apporach}\end{array}}$$
### Amdahl’s Law
Amdahl’s Law calculates the *upper bound* of the speedup when assigning more cores to an application that contains both **serial** *and* **parallel** parts!
$$
\large speedup\leq\frac{1}{{\color{orange} S}+\frac{1-{\color{orange} S}}{{\color{red} N}}}
$$
where ${\color{red} N}$ is the number of cores, ${\color{orange} S}$ is the portion of the application that must be performed serially.

>[!example] 
>${\color{orange} S}=0.25$ (25% of the application is serial $\therefore$ 75% is parallel)
>When ${\color{red} N}=2$ (2 cores), the speedup is no greater than $1.6\times$
>
>If ${\color{red} N}=4$ (4 cores), the upper bound on the speedup is $2.28\times$
>(not $4\times$!)

<canvas height="0" width="0" style="display: block; box-sizing: border-box; height: 0px; width: 0px;"></canvas>
