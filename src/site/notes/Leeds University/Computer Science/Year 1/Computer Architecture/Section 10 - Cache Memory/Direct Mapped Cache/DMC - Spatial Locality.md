---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/computer-architecture/section-10-cache-memory/direct-mapped-cache/dmc-spatial-locality/"}
---

Spatial Locality is the idea that if a memory address is referenced, nearby addresses are likely to be referenced soon
- One-block cache lines don't take advantage of this, therefore:

**We make each cache line two blocks**
Then, we can group the memory addresses into pairs
- i.e. addresses 0 and 1 become ***block address*** 0
$$
Block\ Address \neq Byte\ Address
$$
![Direct-Mapped Cache Block Addresses.png|600](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%2010%20-%20Cache%20Memory/Images/Direct-Mapped%20Cache%20Block%20Addresses.png)
In this example, if a program reads from byte address $4$ we'll load all of memory block $2$ ( Both addresses $4$ and $5$ ) into cache line $2$
- A read from address $5$ will also cause memory block $2$ to be loaded into cache line $2$
![Direct-Mapped Cache Data Placement.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%2010%20-%20Cache%20Memory/Images/Direct-Mapped%20Cache%20Data%20Placement.png)
As a result we must change how the memory address is formatted
![Direct-Mapped Cache Spatial Formatting.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%2010%20-%20Cache%20Memory/Images/Direct-Mapped%20Cache%20Spatial%20Formatting.png)
It is still the same as the [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 10 - Cache Memory/Direct Mapped Cache/Direct Mapped Cache#Stores\|Normal DMC Formatting]] however,
- A final bit is added to choose a block/cache line
- The valid bit is **removed**
- And the address used is the block address *not* the memory address
The [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 10 - Cache Memory/Direct Mapped Cache/Direct Mapped Cache#Loads\|Loading]] function is similarly changed
#### Types of Cache Misses
- Compulsory Miss
	- These misses occur when **the first access** to a block happens
	  As there is no [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 10 - Cache Memory/Direct Mapped Cache/Direct Mapped Cache#^valid-bit\|valid bit]]
- Conflict Miss
	- These misses occur when several blocks are mapped to the same cache line
