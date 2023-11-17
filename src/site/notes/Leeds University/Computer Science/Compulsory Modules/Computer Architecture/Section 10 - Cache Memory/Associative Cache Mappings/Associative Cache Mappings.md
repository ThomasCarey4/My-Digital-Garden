---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/section-10-cache-memory/associative-cache-mappings/associative-cache-mappings/"}
---

#### Fully Associative Mapping
- In fully associative mapping, a main memory block can be loaded into *any* line of cache
	- This way we'll never have a conflict between two or more memory blocks which map to the same cache line
##### The Cost
- Fully associative cache is expensive to implement
	- Because there is no index field in the address anymore, the *entire block* address must be used as the tag
	- Data could be anywhere in the cache, so we must check the tag of every cache line. ***That take a lot of comparators***
