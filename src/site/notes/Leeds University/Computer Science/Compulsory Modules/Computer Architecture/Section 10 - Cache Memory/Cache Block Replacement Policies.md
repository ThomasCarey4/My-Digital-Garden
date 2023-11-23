---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/section-10-cache-memory/cache-block-replacement-policies/"}
---

### Block Replacement Algorithms
Since the cache will fill up, it is necessary to have a strategy for replacing data in cache
- [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 10 - Cache Memory/Direct Mapped Cache/Direct Mapped Cache\|Direct mapping]] is easy - Each blocks only maps to one line
- [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 10 - Cache Memory/Associative Cache Mappings/Associative Cache Mappings\|Associative mapping]] is more flexible, and the following options can be considered (typically implemented via hardware)
	- **Random Choice:** random...
	- **First in First out (FIFO):** Replace the oldest block (The block that was 'first in')
	- **Least Recently Used (LRU):** Replace the block that been ignored the longest
		- (**The most commonly used method**)
	- **Least Frequently Used (LFU):** Replace the block which has had the fewest hits
