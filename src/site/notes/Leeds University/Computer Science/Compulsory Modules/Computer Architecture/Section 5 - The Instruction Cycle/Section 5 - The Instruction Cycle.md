---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/section-5-the-instruction-cycle/section-5-the-instruction-cycle/"}
---

>[!Textbook Reference]
> [Stallings](https://leeds.primo.exlibrisgroup.com/permalink/44LEE_INST/13rlbcs/alma991012536539705181) - 3.1-2
### Programming
- A Program is a sequence of instructions
- For each instruction, an arithmetic or logical operation is performed on some data
- Each distinct operation requires a different set of control signals
### Control Unit
- For each operation a unique code is provided ( **opcode** )
	- e.g. $ADD, MOVE$
- A hardware segment accepts the code, interprets it, and issues the corresponding control signals
### Fetch Cycle
- The ***Program Counter*** ( *PC* ) Holds the address of the next instruction to fetch
- The processor fetches the instruction from the memory location pointed to by the *PC*
- The *PC* is incremented ( unless told otherwise )
- The instruction is loaded into the ***instruction [[Leeds University/Computer Science/Compulsory Modules/Computer Processors/Registers\|register]]*** ( *IR* )
- The processor interprets the instruction and, using the 
  ***accumulator*** ( *AC* ), performs the required actions
### Execute Cycle
- ***Processor $\Longleftrightarrow$ Memory
	- Data transfer between the CPU and main memory
- ***Processor $\Longleftrightarrow$ I/O***
	- Data transfer between the CPU and an I/O module
- ***Data Processing***
	- Performance of an arithmetic or logical operation on the data
- ***Control***
	- Alteration of the sequence of operations,
	  e.g. jump to an out-of-sequence memory location

Combinations of the 4 are also possible
### Program Execution
- The program is started by providing the *PC* with a memory address
- The contents of this address are interpreted as an instruction
	- The [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 4 - Representing Numbers/Definitions/Most Significant Bit\|most significant bits]] provide the ***opcode***
	- The remaining bits give a ***memory address***
	- The contents of this address will be interpreted as data 
	  ( often as an ***operand*** )

