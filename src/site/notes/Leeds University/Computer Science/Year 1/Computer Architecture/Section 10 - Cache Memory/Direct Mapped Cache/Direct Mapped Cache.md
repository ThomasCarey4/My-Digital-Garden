---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/computer-architecture/section-10-cache-memory/direct-mapped-cache/direct-mapped-cache/"}
---

##### Direct Mapped Cache
In **Direct-Mapped Caches** each memory block is assigned to a specific line in the cache
- This makes block placement, lookup and replacement much easier
- Usually used in embedded systems
###### Disadvantages
- While DMC is simple and cheap, it has large problems with its 
{ #Thrashing}

	- If the program attempts to access multiple addresses ( or [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 10 - Cache Memory/Direct Mapped Cache/DMC - Spatial Locality\|blocks]] ) assigned to the same cache line repeatedly, there will be constant 'cache misses'
	- This is known as ***thrashing***

##### How it Works
For example, a simple system would be to map every $n^{th}$ memory address to a cache line, where $n$ is the number of cache lines
![Direct-Mapped Cache.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%2010%20-%20Cache%20Memory/Images/Direct-Mapped%20Cache.png)

The computer may do this by taking the Least Significant Bits
![Direct-Mapped Cache LSBs.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%2010%20-%20Cache%20Memory/Images/Direct-Mapped%20Cache%20LSBs.png)
{ #index}


To distinguish which memory block the cache has copied, you can use a *tag* to supply the rest of the address bits, i.e.
![Direct-Mapped Cache Tags.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%2010%20-%20Cache%20Memory/Images/Direct-Mapped%20Cache%20Tags.png) 
{ #tag}


The computer can the concatenate the tags with the cache line index to calculate the block addresses
![Direct-Mapped Cache Concatenation.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%2010%20-%20Cache%20Memory/Images/Direct-Mapped%20Cache%20Concatenation.png)
###### Valid Bit
Finally, each cache line needs a *valid bit* to inform the system that data has been loaded
- When the system starts the cache would be empty![Direct-Mapped Cache Valid Bit.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%2010%20-%20Cache%20Memory/Images/Direct-Mapped%20Cache%20Valid%20Bit.png) 
#### Loads & Stores in DMC
##### Loads
When the CPU tries to read from memory, the address will be sent to a ***Cache Controller***
- A successful *load* from cache is called a **Cache Hit**
![Cache Controller.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%2010%20-%20Cache%20Memory/Images/Cache%20Controller.png)
A simple *[[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Conjunction\|AND]]* gate is used to confirm the correct memory block is retrieved
##### Stores
- The lowest $k$ bits of the address [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 10 - Cache Memory/Direct Mapped Cache/Direct Mapped Cache#^index\|specify a cache line]]
- The upper $( m \leftrightarrow k )$ address bits are stored in the line's [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 10 - Cache Memory/Direct Mapped Cache/Direct Mapped Cache#^tag\|tag]] field
- Load data from the memory and store it to the data field
- Set the valid bit to 1
![Direct-Mapped Cache Storing.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%2010%20-%20Cache%20Memory/Images/Direct-Mapped%20Cache%20Storing.png)
