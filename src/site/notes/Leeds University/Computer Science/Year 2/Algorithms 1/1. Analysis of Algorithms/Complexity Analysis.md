---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/algorithms-1/1-analysis-of-algorithms/complexity-analysis/"}
---


###### Basic Principles of Complexity Analysis
You can simplify the analysis of algorithms:
- Determine the number of times the basic operations are performed (in the worst case) for an instance of size ***n***
- **Consider a dominating term** in an algorithm’s growth-rate function. The low-order terms can be ignored. If the basic operation is performed ${\color{blue} n^{3}+4n^{2}+3n}$ times, the class of the algorithm is ${\color{red} O(n^{3})}$
- **Ignore a multiplicative constant** in the algorithm’s growth-rate function. If the basic operation is performed ${\color{blue} 5n^{2}}$ times, the class of the algorithm is ${\color{red} O(n^{2})}$
