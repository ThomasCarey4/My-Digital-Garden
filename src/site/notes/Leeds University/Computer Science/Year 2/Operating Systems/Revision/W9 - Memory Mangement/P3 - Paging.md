---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w9-memory-mangement/p3-paging/"}
---


### Motivation
>[!question] Why use a paging memory management technique?
>Previous techniques require the memory to be contiguous, which introduces memory gaps and external fragmentation (requiring compaction).
>Paging allows processes to see contiguous memory space despite the actual data being stored in separate places in the physical memory

**Paging:**
A method that allows processes memory space to be fractured, but still look contiguous from a process’ perspective. Paging is implemented n collaboration between the OS and the hardware. It is in widespread use today!

### The Basic Method
1. Divide the physical memory space into fixed-sized blocks, **frames**
2. Divide the virtual memory space into fixed-sized blocks, **pages**
3. Keep track of all the free frames
4. When a program requires $N$ pages, $N$ free frames have to be found
5. Each process’ **page table** maps their pages to frames (**virtual address** $\rightarrow$ **physical address**)

>[!abstract] Virtual Addresses
>![Pasted image 20250122114349.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/W9%20-%20Memory%20Mangement/images/Pasted%20image%2020250122114349.png)
>When the CPU makes a call to an address, it uses the page number and the page offset, the page number is then used (with the page table) to find the frame, where with the page offset the specific byte is found
>![Pasted image 20250122114609.png|500](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/W9%20-%20Memory%20Mangement/images/Pasted%20image%2020250122114609.png)

#### Paging
Key remarks about paging:
- No external fragmentation: Any free frame an be allocated to a process
- Internal fragmentation present:
	- The process might not need the entire page

>[!abstract] Page Sizes
>Today pages are typically $4$ or $8$ KB in size. Some systems support two page sizes which includes an option for **huge pages**

#### Frame Allocation to Pages
The main steps are:
1. The process requiring execution arrives in the system
2. The size, in terms of pages, is determined: $\large\lceil\frac{\texttt{size}}{\texttt{pagesize}}\rceil$ (Number of pages required)
3. Each page requires a frame in physical memory
4. If a process requires $N$ pages, $N$ frames need to be available
5. The first page is loaded into an allocated frame
6. The frame number is written into the page table
7. Repeat steps **6** and **7** until all the pages are copied into frames and the page table of the process is fully set up. The process can then start and use logical addresses

>[!abstract] A programmer’s view of memory
>Paging allows the programmer’ view of memory to be separated from the physical memory. The programmer sees a contiguous area of memory available for a particular program. In reality, the program is scattered across physical memory, with frame sitting amongst frames of other programs

#### Implementation
Each process has a page table stored in main memory
- The **P**rocess **C**ontrol **B**lock of each process stores the address of the page table
- When the scheduler selects a process, it must set up the hardware page table by getting the copy from the memory
	- Simple hardware page table:
		- A set of high-speed registers
		- Fast translation of logical addresses
		- Context switch time increases because these register have to be exchanged

>[!abstract] PTBR Register
>Most CPUs support large tables (for example $2^{20}$ entries)—the register approach not feasible. Instead, page tables are kept in memory and the **page table base register (PTBR)** points to it.
>- Context switches only requires one register swap

### Translation Look-Aside Buffers
**Page tables in memory**:
When page tables are stored in memory, process data/instruction access requires two memory operations, one for the page tables and another for the actual data

>[!abstract] Translation look-aside buffers
>The technique, also called **associative memory**, provides fast memory for storing commonly accessed frame addresses, typically $32$ to $1024$ entries. When the CPU access memory, the MMU first checks if the page number is in the **TLB** and uses it if so. Otherwise (**TLB miss**) it gets the frame number from memory and updates the **TLB**

>[!abstract] TLBs in practice
>Modern CPUs typically provide multiple levels of TLBs.
>For example, the Intel Cor i7 has a 128-entry L$1$ instruction TLB and a 64-entry data TLB.
>- If a TLB miss occurs, it checks the 512-entry L$2$ TLB.
>- In case of another TLB miss, the page table in the main memory is looked at

#### Memory Protection with Pages
Page tables can contain two extra bits, one for R/W access control and one for Valid/Invalid control (i.e. whether that frame actually contains the page)

>[!abstract] Page-Table Length Register
>Instead of storing unused pages we may have a **PTLR** register that stores the size of the page table (number of pages). This can be used for memory protection together with the **PTBR** by ensuring the process only uses the amount of memory its been allocated

#### Shared Pages
Paging allows for efficient sharing of code between processes
- **Reentrant code** means that the code of the library is not self-modifying
	- All processes can read it at the same time
	- For example, with shared pages there is no need to have the copy of the `libc` C standard library in each processes’ memory

#### Hierarchical Paging
![Pasted image 20250122124507.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/W9%20-%20Memory%20Mangement/images/Pasted%20image%2020250122124507.png)
The first table contains entries that point to *a* table that then points to the memory
>[!abstract] 64-bit Architectures
>For 64-bit architectures even the two-level hierarchical page table requires too many entries. Other solutions are **hashed page tables** and **inverted page tables**

