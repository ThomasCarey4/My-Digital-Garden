---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/computer-architecture/section-4-representing-numbers/floating-point/"}
---

##### Typical Format:
- 32 bits
- The first bit is the ***sign bit***, 0 for positive
- The next 8 bits represent the exponent, in ***[[Leeds University/Computer Science/Year 1/Computer Architecture/Section 4 - Representing Numbers/127-Bias Notation\|127-Bias Notation]]***
- This leaves 23 bits for the mantissa

This format will be able to represent numbers in the range $\approx10^{-38}\to10^{38}$ 
With approximately 7 decimal digits of precision