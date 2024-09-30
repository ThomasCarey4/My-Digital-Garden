---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/computer-architecture/section-9-memory/definitions/checksum/","tags":["Definition"]}
---

- A **checksum** is a form of **error detection** code
	- It is usually an affix to a piece of data, created through running an algorithm on the data
	-  
<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/computer-architecture/section-9-memory/definitions/hamming-distance/#example" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



- For example, a simple [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 9 - Memory/Definitions/Checksum\|Checksum]]: 

</div></div>

- It is a form of **redundancy**
	- Information redundancy: If packet is valid, the checksum is unnecessary
	- Partial Redundancy: If packet is invalid, the packet cannot be reconstructed from the checksum
- If the checksum is **"strong enough"** ( i.e. has a high minimum [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 9 - Memory/Definitions/Hamming Distance\|Hamming Distance]] )  it is possible to reconstruct a "most likely" correct packet
	- In this case the partial redundancy is removed