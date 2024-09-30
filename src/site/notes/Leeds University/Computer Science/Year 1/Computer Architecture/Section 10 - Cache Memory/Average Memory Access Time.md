---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/computer-architecture/section-10-cache-memory/average-memory-access-time/","tags":["Definition"]}
---

$$
\text{AMAT} = \text{Hit Time}\ +\ (\ \text{Miss Rate}\ \times\ \text{Miss Penalty}\ )
$$ 
{ #Equation}


##### Improving AMAT
- Keep *Miss Rate* low
	- Increased cache size lowers cache *Miss Rate*, but this increases *Hit Time*
	- **Better cache management policies:**
		- Prefetching: Anticipate what you will need
		- Replacement: Anticipate what you don't need
- Keep *Miss Penalty* low
	- Reduce miss penalty with a faster main memory ( but higher cost )
	- Better solved by adding intermediate levels
