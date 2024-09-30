---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/computer-architecture/section-9-memory/definitions/parity-bit/","tags":["Definition"]}
---

- Using a ( redundant ) bit to detect and correct a one-bit error
- E.g. count the number of bits that are 1, see if it's odd or even
	- Parity is 0 if the number of 1 bits is odd
	- $0110 \rightarrow$ parity bit is 1
	- $1000 \rightarrow$ parity bit is 0
	- Parity can detect a single error, but can't tell you which of the bits got flipped
