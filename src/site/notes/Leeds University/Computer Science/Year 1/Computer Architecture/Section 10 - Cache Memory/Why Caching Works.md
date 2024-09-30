---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/computer-architecture/section-10-cache-memory/why-caching-works/"}
---

Memory hierarchy exploits program locality
- Programs tend to reference parts of their address space that are local in $\color{red}\text{time}$ and $\color{red}\text{space}$
##### Temporal Locality
Recently referenced addressed are likely to be referenced again - reused
##### Spatial Locality
If a memory address is referenced, nearby addresses are likely to be referenced soon
- E.g. access to array $A[1]$ is likely to be followed by an access to $A[2]$
