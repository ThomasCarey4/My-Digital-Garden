---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w9-memory-mangement/p2-contiguous-memory-allocation/"}
---


>[!abstract] Contiguous Memory Allocation
>OS and processes have to live in memory in order to all run concurrently, requiring efficient allocation of their memory areas. Contiguous allocation of the memory space is one way to implement this

Partition the memory into two parts:
1. The area for the Operating System
2. The area for Processes, stored in single contiguous blocks

>[!warning] Need for Memory Protection
>Need to protect the OS and processes, that are stored in the same memory space, from each other

### Memory Allocation#
The OS must keep track of free and occupied partitions
- At the start, memory is one big free block
- The OS allocates **variable size partitions** as required
- This causes **Memory holes** of variable size form
- When a process exits, it leaves a memory hole that is merged with adjacent holes

Given an allocation request of $N$ bytes, how to determine which memory hole to return?
- **First-fit**: Allocate the first free memory area of size $N$ or larger (from the bottom)
- **Best-fit**: Search the list of free memory areas and allocate the smallest that fits $N$ bytes (best case scenario is we find a memory hole of $N$ bytes)
- **Worst-fit**: Allocate the largest free memory area available of size at least $N$

>[!abstract] Internal Fragmentation
>Allocated memory is larger than $N$, the requested size!
>- The extra bytes in the allocate block are unused
>- This arises when memory is split into fixed-sized partitions

>[!abstract] External Fragmentation
>$N$ bytes exist to satisfy the request for memory, but the space is not contiguous.
>- The memory is broken in to many small pieces

#### Reducing External Fragmentation
**Compaction:**
Shuffle the memory contents to merge all the free memory holes into one contiguous space. Dynamic relocation is required for this to work, during execution.
- Requires moving the program and data and updating the relocation register to reflect the change in the starting address
