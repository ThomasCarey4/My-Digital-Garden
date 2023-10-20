---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/section-4-representing-numbers/127-bias-notation/"}
---

Exponent is stored in ***biased notation***
- Bias 127 means that we use the numbers 0 to 255 in order to represent the numbers -127 to 128
- In order to calculate the biased notation, we add 127 to the true exponent which we wish to store
##### Example
| Exponent | $\to$ |Representation |
| :--: | :--: | :--: |
|-127 || 0 |
| -1 || 126 |
| 0 || 127 |
| 128 || 255 |
