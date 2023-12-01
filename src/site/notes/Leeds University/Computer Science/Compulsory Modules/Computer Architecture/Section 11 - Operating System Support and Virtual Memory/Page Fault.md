---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/section-11-operating-system-support-and-virtual-memory/page-fault/","tags":["Definition"]}
---

>[!important] 
>>[!question] 
>>What if a piece of data is on disk rather than in memory?
>>- If the [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table\|Page Table]] indicates that the virtual address is not in memory
>
>A hardware exception will be generated (captured by the OS)
>- The current process suspends, others can resume
>- The OS moves the data to memory and resumes the suspended process
{ #Example}

#TODO 
