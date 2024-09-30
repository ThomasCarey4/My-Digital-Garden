---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/computer-architecture/section-8-cpu-structure-and-pipelining/section-8-cpu-structure-and-pipelining/"}
---

#TODO He do be skipping like half the slides lol
### [[Leeds University/Computer Science/Year 1/Computer Processors/Registers\|Registers]]
- The CPU must have some working space
    ( temporary storage )
- This space is called a **[[Leeds University/Computer Science/Year 1/Computer Processors/Registers\|register]]**
- The number and function vary between processor designs
- This is one of the major design decisions
- Top level of memory hierarchy
#### Control and Status [[Leeds University/Computer Science/Year 1/Computer Processors/Registers\|Registers]]
- *PC*
	- Program Counter
- *IR*
	- Instruction [[Leeds University/Computer Science/Year 1/Computer Processors/Registers\|Register]]
- *MAR*
	- Memory Address [[Leeds University/Computer Science/Year 1/Computer Processors/Registers\|Register]]
- *MBR*
	- Memory Buffer [[Leeds University/Computer Science/Year 1/Computer Processors/Registers\|Register]]
#### General Purpose [[Leeds University/Computer Science/Year 1/Computer Processors/Registers\|Registers]]
- May be true general purpose
- May be restricted
- May be used for data or addressing
- Data
	- Accumulator
- Addressing
	- Address of a base of a Segment
##### How Many GP [[Leeds University/Computer Science/Year 1/Computer Processors/Registers\|Registers]]?
- Between 8-32
- Fewer = More memory references
- How big?
	- Large enough to hold a full address
	- Large enough to hold a full [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 9 - Memory/Definitions/Machine Word\|Machine Word]]
- Often possible to use two data [[Leeds University/Computer Science/Year 1/Computer Processors/Registers\|Registers]] for one [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 9 - Memory/Definitions/Machine Word\|Machine Word]]/address
#### Program Status [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 9 - Memory/Definitions/Machine Word\|Machine Word]] [[Leeds University/Computer Science/Year 1/Computer Processors/Registers\|Register]]
- The *PSW* is a special [[Leeds University/Computer Science/Year 1/Computer Processors/Registers\|register]] that contains status information
- This typical includes **condition codes** such as:
	- Zero ( When the result is zero )
	- Carry
	- Overflow
	- Interrupt enable/disable
### Instruction Cycle
#### Data Flow
##### Instruction Fetch
This depends on the precise CPU design
In general, the **fetch** consists of
1. *PC* contains the address of next instruction
2. Address is moved to *MAR*
3. Address is placed on address bus
4. Control unit requests memory read
5. Result is placed on data bus, copied to *MBR*, then to *IR*
6. Meanwhile *PC* is incremented by 1
##### Data Fetch
- The *IR* is examined
- If indirect addressing is used, an *Indirect Cycle* is performed
	- Right most N bits of *MBR* transferred to *MAR*
	- Control Unit request memory read
	- Result ( address of operand ) moved to *MBR*
##### Indirect Cycle
#TODO 

---
### Prefetching and Pipelining
#### Prefetch
- A fetch accesses main memory
- An execution usually does not access main memory
- Therefore we can fetch the next instruction at the same time as executing the current instruction
- This is called **Instruction Prefetch**
#### Pipelining
| Code | Description |
| :-: | :-: |
| FI | Fetch Instruction |
| DI | Decode Instruction |
| CO | Calculate Operands ( effected addressed ) |
| FO | Fetch Operands |
| EI | Execute Instructions |
| WO | Write Result |
**Pipelining** means overlapping these operations
##### Timing
![Pipeline Timing.png|500](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%208%20-%20CPU%20Structure%20and%20Pipelining/Pipeline%20Timing.png)
##### Multiple Streams
- Have two pipelines
- Prefetch each branch into separate pipeline
- Use appropriate pipeline
- Leads to bus and [[Leeds University/Computer Science/Year 1/Computer Processors/Registers\|register]] contention
- Multiple branches lead to further pipelines being needed
