---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/section-11-operating-system-support-and-virtual-memory/page-fault/","tags":["Definition"]}
---

>[!important] 
>>[!question] 
>>What if a piece of data is on disk rather than in memory?
>>- If the [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Page Table\|Page Table]] indicates that the virtual address is not in memory
>
>A hardware exception will be generated (captured by the OS)
>- The current process suspends, others can resume
>- The OS moves the data to memory and resumes the suspended process
{ #Example}

Page faults are generated when the [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Page Table\|Page Table]] tells the OS that the page is on **disk**
	- The CPU then generates a ***Page Fault Exception***
- The OS must then retrieve the data from the disk
		- The OS chooses a page to **evict** from **[[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/RAM\|RAM]]** and write to **disk**
		- The OS then reads the page from **disk** and puts it in **[[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/RAM\|RAM]]**
		- The OS then updates the **[[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Page Table\|Page Table]]** to map the new page
- The OS then jumps back to the instruction that caused the page fault
		- This time won't cause a page fault since the page has been loaded into memory

