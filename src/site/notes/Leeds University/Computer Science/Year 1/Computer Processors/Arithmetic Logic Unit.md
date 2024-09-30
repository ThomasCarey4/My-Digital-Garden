---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/computer-processors/arithmetic-logic-unit/"}
---

The **Arithmetic Logic Unit** (**ALU**) is the centrepiece of any modern day computer
- ALUs implement a fixed set of functions
- Each function can take at most two multi-bit arguments
- The ALU outputs the result of the boolean function and a set of flags
![ALU.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Processors/images/ALU.png)
- The instruction is a set of control bits which select which function the ALU should output
	- [[Leeds University/Computer Science/Year 1/Fundamental Math Concepts/Fundamentals of Logic/Propositional Logic/Connectives/Conjunction\|And]]
	- Adder
	- Pre/post processing on inputs/outputs
Our specific ALU accepts
- Two **16**-bit wide arguments
- A **6**-bit wide instruction
And outputs
- a **16**-bit wide output
- A bit to indicate if the output is **0**
- A bit to indicate o the output is less than **0**

White a **6**-bit wide instruction gives the ALU a possible $\color{blue} 2^{6}$ instructions
- We are only interested in **18** of them

#### Control Bits
The ALU has the choice between two basic functions, logical **And** and **Addition**
- All operations are multi-bit operations

| Bit | Description                       |
| :-: | --------------------------------- |
| za  | Zero input **A**                  |
| na  | Negate input **A**                |
| zb  | Zero input **B**                  |
| nb  | Negate input **B**                |
|  f  | Selection between **&** and **+** |
| no  | Negate **output**                 |
###### Example

|     | za  | na  | zb  |            nb            |  f  | no  | output |
| --- | :-: | :-: | :-: | :----------------------: | :-: | :-: | :----: |
|     | *0* | *0* | *1* |           *1*            | *1* | *0* | *a-1*  |
| a   |  a  |  a  |  a  |            a             | a-1 | a-1 |  a-1   |
| b   |  b  |  b  |  0  | -1<br>$\small(11111111)$ |  ^  |  ^  |   ^    |
#### Implementation
Notice that the **ALU** is composed of
- A logic circuit that can negate or zero an input (twice)
- Logic circuits for **Addition** and **And**
- A logic circuit to select between them
- A logic circuit to negate the output
- A logic circuit to handle flags

