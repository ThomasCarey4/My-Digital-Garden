---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/algorithms-1/1-analysis-of-algorithms/logarithmic-algorithms/"}
---


Rules of Logarithms

| Exponent                            | Logarithm                                     |
| ----------------------------------- | --------------------------------------------- |
| $b^{k}\times b^{\ell}=b^{k+\ell}$   | $\log_{b}(xy)=\log_{b}x+\log_{b}y$            |
| $\frac{b^{k}}{b^{\ell}}=b^{k-\ell}$ | $\log_{b}(\frac{x}{y})=\log_{b} x-\log_{b} y$ |
| $(b^{k})^{\ell}=b^{k\ell}$          | $\log_{b}(x^{\ell})=\ell\log_{b}x$            |
|                                     | $\log_{b}x=log_{b}(a)\times\log_{a}(x)$       |
###### Typical Algorithms
Where $k$ = The number of iterations:
```python
i = 1
while i < n do
   i = i * 2
```
The algorithm stops after iteration $k$ when $i$ reaches $2^{k},2^{k}\geq n$
```python
i = n
while i > 1 do
   i = i / 2
```
The algorithm stops after iteration $k$ when $i$ reaches $n/2^{k},n/2^{k}\leq 1$

>[!tip] 
>Assume $2^{k-1}<n\leq 2^{k}$
>This implies $k=\lceil\log_{2}n\rceil$

