---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/computer-architecture/section-10-cache-memory/cache-block-replacement-policies/"}
---

### Block Replacement Algorithms
Since the cache will fill up, it is necessary to have a strategy for replacing data in cache
- [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 10 - Cache Memory/Direct Mapped Cache/Direct Mapped Cache\|Direct mapping]] is easy - Each blocks only maps to one line
- [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 10 - Cache Memory/Associative Cache Mappings/Associative Cache Mappings\|Associative mapping]] is more flexible, and the following options can be considered (typically implemented via hardware)
	- **Random Choice:** random...
	- **First in First out (FIFO):** Replace the oldest block (The block that was 'first in')
	- **Least Recently Used (LRU):** Replace the block that been ignored the longest
		- (**The most commonly used method**)
	- **Least Frequently Used (LFU):** Replace the block which has had the fewest hits
### Write Policies for Caches
##### Reads and Writes in a Cache
- CPU wants to read:
	- **Cache Hit**
	- **Cache Miss**
		- Evict a block
- CPU wants to write:
	- **Write Hit:** Cache contains the block
	- **[[Leeds University/Computer Science/Year 1/Computer Architecture/Section 10 - Cache Memory/Cache Block Replacement Policies#Write Miss\|#Write Miss]]:** Cache does not contain the block
#### Write-Through Caches
Update both the cache and main memory for each write
- This prevents errors where the cache holds a different value to the memory
- Much slower as memory [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 9 - Memory/Definitions/Access Time\|Access Time]] is much higher than the cache's
	- As a result, it is handled by a microcontroller to prevent slowing the CPU down
#### Write-Back Caches
The memory is not updated until the cache block needs to be replaced
- Needs a dirty bit in the cache to mark the inconsistency
{ #Dirty-Bit}

- Subsequent reads to the same memory address will be served by the cache
- As a result, the memory is not updated until the reference inside the cache is evicted

#### Write Miss
What if the memory address we want to write to is not loaded into cache?
##### Allocate on Write
This strategy loads the newly written data into the cache
- Good if the data to be written will be used soon
##### Write Around
The write operation goes directly to main memory without affecting the cache
- Good when data will not immediately be used again
- Some modern processors with write-allocate cache provide special store instructions called **non-temporal stores** to do this
	- Some processors also have different levels of memory (L1, L2, L3) which each have different methods
