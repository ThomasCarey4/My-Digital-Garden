---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w6-threads-and-concurrency/p3-libraries-for-multithreading/"}
---


### Multithreading Models
![Pasted image 20250120185924.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120185924.png)
Support may be provided for threads at user level and kernel level: **user threads** and **kernel threads**

User threads work in user mode and kernel threads require direct OS support
#### Many-to-One
![Pasted image 20250120190032.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120190032.png)
**Disadvantage:** The entire process blocks if one threads calls a blocking system call. Multiple threads are unable to run in parallel $\rightarrow$ very few systems implement this
#### One-to-One
![Pasted image 20250120190125.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120190125.png)
**Advantages:** 
- Another thread can run when once calls a blocking system call
- Parallel processing possible!
**Disadvantage**: Each user thread *requires* creating a kernel thread. Performance may suffer :(
#### Many-to-Many
![Pasted image 20250120190301.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120190301.png)
**Advantages**: 
- The number of kernel threads customisable according to application or machine requirements
- Number limited; does not depend on how many user threads exist
- The kernel can run threads in parallel
#### Two-Level-Threads
![Pasted image 20250120190446.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120190446.png)
A combined approach while allows specific user threads to be assigned a kernel thread, but still multiplex between other user and kernel threads
### Thread Libraries
A thread library provides an API for managing threads
Two possible approaches:
- Entirely in **User Mode**
- Entirely in **Kernel Mode**
Three main libraries:
- POSIX Pthreads
- Windows Thread Library
- Java Thread API
>[!tip] 
>For Pthreads and Window data declared globally is shared among threads

>[!abstract] Synchronous and Asynchronous Threading
>In **asynchronous threading**: The parent continues working concurrently with any children created.
>In **synchronous threading**: The parent waits for its children to complete:
>	- For example, the parent may combine the results from its children

#### Pthreads
Pthreads is a standard API for thread creation and synchronisation
	- Various IEEE standards address it
	- It is a **specification *not* an implementation**
OS designers can implement the specification their own way
```c
#include <pthread.h>
#include <stdio.h>
#include <stdlib.h>

int sum;
void *runner(void *param);

int main(int arc, char *argv[]) {
	pthread_t tid;
	pthread_attr_t attr;
	
	// Create a thread
	pthread_attr_init(&attr);
	pthread_create(&tid, &attr, runner, argv[1]);
	
	// Wait for the thread to exit
	pthread_join(tid, NULL);
	
	printf("sum = %d\n", sum);
}

void *runner(void *param) {
	int i, upper = atoi(param);
	sum = 0;
	for (i = 1; i <= upper; i++) {
		sum += i;
	}
	pthread_exit(0);
}
```
Here, sum is a global variables (accessible by both threads) and runner is executed in a separate thread to main.
$$\boxed{\begin{array}{c}\text{Look into Window and Java threading}\end{array}}$$
### Implicit Threading
Designing parallel programs manually is potentially a cumbersome task.

A better way support to the design of concurrent and parallel applications is to automate the identification and creation of threads

Offload this work form developers to compilers: **implicit threading**

>[!abstract] Advantage of Implicit Threading
>The developer identifies **tasks** that can run in parallel. The environment determines the low-level details of thread creation and management

#### Thread Pools
Manual thread creation has two problems:
- Thread creation may be costly; threads are discarded once finished
- The number of threads is unbounded: May exhaust system resources
>[!abstract] Thread Pools
>Create a number of threads at startup and make them available for doing work. The application requests resources from the thread pool: If there is a thread available, it is allocated; otherwise the app waits until a thread is placed back into the pool

Several advantages of thread pools:
- Servicing a request with existent an existent thread may be faster than creating and deleting threads
- The thread pool limits the number of threads
- The thread pool can be configured based on available resources, or adjusted dynamically based on what the applications are doing

![Pasted image 20250120193449.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250120193449.png)
The fork-join model works for implicit threading as well:
1. A library manages the threads and assignment of tasks to threads
2. Threads are not created directly during forks. Parallel tasks are identified and allocated to threads
3. The join mechanism provides the synchronicity
#### Example Libraries
- The fork-join library is available in the Java API
- **OpenMP** is a way to augment C, C++, Fortran programs to identify what can be parallelised
- **Grand Central Dispatch** is an Apple technology for implicit threading
	- What a goofy name lol
- **Intel Thread Building Blocks** supports designing parallel C++ programs
- **CUDA** allows you to program NVIDIA Graphics Cards to perform massively parallel computations
##### OpenMP Example in C
```c
#include <omp.h>
#include <stdio.h>

int main(int argc, char *argv[]) {
	// Sequential Code
	
	printf("I am in a sequential region.\n");
	
	#pragma omp parallel {
		printf("I am a parallel region %d.\n", omp_get_thread_num());
	}
	
	/* Sequential Code */
	printf("Second sequential region.\n");
	
	return 0;
}
```

When wanting to parallelise a for loop (assuming each iteration is independent), you can do:
```c
#pragma omp parallel for {
	for (i = 0; i < N, i++) {
		c[i] = a[i] + b[i];
	}
}
```
- Take two array $a$ and $b$ of size $N$. We want to add the arrays and produce a new array $c$.
	- Vector addition…
- This is an **embarrassingly parallel** problem
	- Yes that is a technical term lol
- OpenMP `#pragma` will divide the work among the threads it assigns from **its** thread pool
- Different parts of the vectors will be added in parallel
>[!abstract] Other OpenMP Features
>Developers can choose several levels of parallelism. For example, you can set the number of threads manually. It also allows you to say whether data is shared or private among threads

