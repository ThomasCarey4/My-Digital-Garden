---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/section-11-operating-system-support-and-virtual-memory/virtual-memory/"}
---

Virtual Memory: *Indirection to physical memory*
	- The program uses a **virtual memory address** (program address)
	- The virtual memory address is converted into a **physical address** (real address) [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Page Table\|{1}]]
	- The physical address indicates a physical location of data
	- Physical location can be memory or disk
```mermaid
graph LR
V[Virtal: 5000] --> D[Disk: 9100]
```
##### Motivation
- Physical memory is much larger than [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/RAM\|RAM]] or Cache
- Virtual memory allows memory to appear bigger for running programs
- Support for memory sharing, protection, etc
- Allow a process to exist in non-contiguous memory
	- Avoid memory fragmentation
#### Page Faults
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/computer-architecture/section-11-operating-system-support-and-virtual-memory/page-fault/#37db08" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




>[!important] 
>>[!question] 
>>What if a piece of data is on disk rather than in memory?
>>- If the [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Page Table\|Page Table]] indicates that the virtual address is not in memory
>
>A hardware exception will be generated (captured by the OS)
>- The current process suspends, others can resume
>- The OS moves the data to memory and resumes the suspended process

Page faults are generated when the [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Page Table\|Page Table]] tells the OS that the page is on **disk**
	- The CPU then generates a ***Page Fault Exception***
- The OS must then retrieve the data from the disk
		- The OS chooses a page to **evict** from **[[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/RAM\|RAM]]** and write to **disk**
		- The OS then reads the page from **disk** and puts it in **[[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/RAM\|RAM]]**
		- The OS then updates the **[[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Page Table\|Page Table]]** to map the new page
- The OS then jumps back to the instruction that caused the page fault
		- This time won't cause a page fault since the page has been loaded into memory



</div></div>

#### Separate Address Spaces
Each address has its own virtual address space
The OS controls how these virtual addresses are mapped to physical memory
	- E.g., virtual address $0100$ for processes 1 and 2 could be mapped onto different physical locations
![Virtual Address Spaces.png|600](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Architecture/Section%2011%20-%20Operating%20System%20Support%20and%20Virtual%20Memory/Images/Virtual%20Address%20Spaces.png)
#### Memory Protection
Each [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Page Table\|Page Table]] entry contains access rights information
	- This is hardware enforced (An exception will be triggered if violated)
![Memory Protection.png|600](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Architecture/Section%2011%20-%20Operating%20System%20Support%20and%20Virtual%20Memory/Images/Memory%20Protection.png)
#### Virtual Memory vs Caches
Virtual memory is like a cache, but with a different purpose
	- Cache - Performance goals
	- Virtual Memory - Programmability / Multi-programming goals
Cache lines are called **Pages** in virtual memory
- A virtual address consists of
	- A virtual page number
	- A page offset field (less-significant bits)
![Virtual Address.png|400](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Architecture/Section%2011%20-%20Operating%20System%20Support%20and%20Virtual%20Memory/Images/Virtual%20Address.png)
#### Pages and Frames
Physical memory is organised into **Frames** and virtual memory into **Pages**
	- **Page** = Block of consecutive **virtual** memory
	- **Frames** = Block of consecutive **physical** memory
When a process is created:
	- The OS allocates the required number of frames to it
	- The OS maintains the list of free frames
	- The [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Page Table\|Page Table]] is used to keep track
#### Summary of Virtual Memory
Virtual memory adds a level of **indirection** between the **virtual program addresses (VA)** and the **physical [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/RAM\|RAM]] addresses (PA)**
This allows us to
	- Map memory to disk ("Unlimited" memory to run larger programs)
	- Keep programs from accessing each other's memory (Memory protection)
	- Fill holes in the [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/RAM\|RAM]] address space (Efficiency)
- But **we have to translate every single memory access** from a **VA** to a **PA**
		- **Page tables** for each process to keep track of all translations
		- Fast translation via a hardware **[[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Translation Look-Aside Buffer (TLB)\|Translation Look-Aside Buffer (TLB)]]**
