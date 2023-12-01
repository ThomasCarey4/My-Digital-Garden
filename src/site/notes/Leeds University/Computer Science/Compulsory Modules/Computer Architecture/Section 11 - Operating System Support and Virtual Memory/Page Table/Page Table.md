---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/section-11-operating-system-support-and-virtual-memory/page-table/page-table/","tags":["Definition"]}
---

#TODO 
### Page Table Entries

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/computer-architecture/section-11-operating-system-support-and-virtual-memory/page-table/page-table-entry-pte/#definition" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



You have one **[[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Page Table\|Page Table]] Entry** (PTE) for each page of the [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Virtual Memory\|virtual memory]]
![Page Table Entry.png|600](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Architecture/Section%2011%20-%20Operating%20System%20Support%20and%20Virtual%20Memory/Images/Page%20Table%20Entry.png) 

</div></div>

##### Address Translation
![Address Translation.png|600](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Architecture/Section%2011%20-%20Operating%20System%20Support%20and%20Virtual%20Memory/Images/Address%20Translation.png)
#### Demand Paging
Do not require all pages of a process in memory
- Bring in pages as required
![Demand Paging.png|500](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Architecture/Section%2011%20-%20Operating%20System%20Support%20and%20Virtual%20Memory/Images/Demand%20Paging.png)


<div class="transclusion internal-embed is-loaded"><div class="markdown-embed">



### Translation Look-Aside Buffer (TLB)
The **TLB** is a hardware cache for [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Page Table\|page table]] entries
	- It contains the [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 11 - Operating System Support and Virtual Memory/Page Table/Page Table Entry (PTE)\|PTEs]] that have been most recently used
	- Works like a data cache


</div></div>
