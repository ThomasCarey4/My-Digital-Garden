---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/section-10-cache-memory/associative-cache-mappings/set-associative-mapping/"}
---

- Combine the benefits of [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 10 - Cache Memory/Direct Mapped Cache/Direct Mapped Cache\|direct]] and [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 10 - Cache Memory/Associative Cache Mappings/Associative Cache Mappings\|fully associative mappings]]
- Divide the cache lines into groups, called **[[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|5.1 Sets]]**
	- Each memory block is mapped into one [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] in the cache (direct mapping for [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|5.1 Sets]]), but the block may be placed in any cache line within that [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] (fully associative within a [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]])
	- If each [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|set]] has $k$ lines, the cache is a $k$-way associative cache.

![Set Associative Mapping Addresses.png](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Architecture/Section%2010%20-%20Cache%20Memory/Images/Set%20Associative%20Mapping%20Addresses.png)
![Set Associative Mapping Diagram.png](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Architecture/Section%2010%20-%20Cache%20Memory/Images/Set%20Associative%20Mapping%20Diagram.png)
