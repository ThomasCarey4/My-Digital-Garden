---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w9-memory-mangement/p4-memory-swapping/"}
---


### Standard Swapping
Process instructions and data have to reside in memory for execution
- When not executing, a process can be swapped out into disc and brought back into memory later
- Why? When main memory is at its limit, to make space for something with higher priority
- **Swapping** allows for the total memory to look larger than the available physical memory
- If $N$ processes are executing, but only $N/2$ can fit into memory, the users still see that all $N$ are working even though half of them are swapped out into the disc

With paging, when memory is swapped back in, the page table(s) have to be updated to match the new configuration

### Swapping in Mobile Systems
Most Operating Systems on PCs and high-performance computers support swapping with pages
However, on mobile systems this is typically not available
- On mobile systems flash memory is used instead of large hard drives
- Space limitations and flash memory degradation due to writing operations make swapping not practical.
- Instead, iOS for example ask applications to release some memory
	- They may also forcibly terminate some old processes when out of memory

