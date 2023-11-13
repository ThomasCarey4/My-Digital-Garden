---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/section-9-memory/definitions/hamming-distance/","tags":["Definition"]}
---

- Between 2 strings of bits
	- The number of bit positions in which 2 strings differ
	- E.g. the distance between $1011101 \rightarrow 1001001$
		- is 2 as $10\color{red}0\color{white}1\color{red}0\color{white}01$
- Minimum Hamming Distance of a code
	- If distance is $d$, then $d\textendash \textrm{single}$ bit errors are required to convert any one valid code ( string ) into another code with the same [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/Checksum\|checksum]]
- For example, a simple [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/Checksum\|checksum]]:
{ #example}

	- Data of 8 bits:
		- $\boxed{0110}\ \boxed{1010}$
	- [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/Checksum\|Checksum]] of 4 bits:
		- XOR the two 4-bit blocks $\to\boxed{1100}$
- What is the minimum hamming distance of this code?
If one bit changes, the XOR will always result in a different [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/Fundamentals of Logic/Definitions/Truth Value\|truth value]] due to its nature
However, if the same two bits change ( i.e. the 3rd bit in the first block and the 3rd bit in the second ) then the XOR value will not change and therefore the [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/Checksum\|checksum]] would be valid
As a result the minimum hamming distance must be 2, as with 2 errors you can still get a valid [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/Checksum\|checksum]]