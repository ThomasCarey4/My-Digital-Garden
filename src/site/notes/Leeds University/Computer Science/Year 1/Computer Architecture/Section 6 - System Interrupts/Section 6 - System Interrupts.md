---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/computer-architecture/section-6-system-interrupts/section-6-system-interrupts/"}
---

Computers provide a mechanism by which other modules may interrupt the normal processing sequence
- Some devices can be many orders of magnitude slower than the CPU
- **Interrupts** allow the CPU to work, pausing to service external devices only when they signal that they require attention
- The processor and operating system are responsible for suspending and resuming the user program appropriately

#### Common Classes of Interrupts
- Program
	- e.g. overflow, division by zero
- Timer
	- Generated by internal processor timer
- I/O
	- An I/O controller signals operation completion
- Hardware Failure
	- e.g. power failure, memory parity error
### Flow Control
Consider a program which is intermittently required to write data
- This is done by a separate I/O program with its own preparation and completion operations
- Interrupts allow this to be done efficiently 
- The main program may still be required to wait
![Program Flow Control.png|700](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%206%20-%20System%20Interrupts/Program%20Flow%20Control.png)
### Interrupt Cycle
As part of the instruction cycle the processor checks for an interrupt signal
- If there's no interrupt, fetch the next instruction
- If an interrupt is pending:
	- Suspend execution of the current program and save its "state",
	- Set the *PC* to the start address of the **interrupt handler** routine and process the interrupt,
	- Restore the previous state and continue the interrupted program
### Augmented Instruction Cycle
![Augmented Instruction Cycle 1.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%206%20-%20System%20Interrupts/Augmented%20Instruction%20Cycle%201.png)
![Augmented Instruction Cycle 2.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%206%20-%20System%20Interrupts/Augmented%20Instruction%20Cycle%202.png)
### Multiple Interrupts
###### Approach 1: Disabled interrupts ( sequential )
- The processor ignores further interrupts whilst processing one interrupt
- Ignored interrupts remain pending and are checked after the first interrupts has been processed
- Interrupts are handled in the sequence as they occur
![Sequential Interrupts.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%206%20-%20System%20Interrupts/Sequential%20Interrupts.png)
###### Approach 2: Define Priorities ( nested )
- Low priority interrupts can be interrupted by higher priority interrupts
- When the higher priority interrupt has been processed the processor returns to the previous interrupt
![Nested Interrupts.png](/img/user/Leeds%20University/Computer%20Science/Year%201/Computer%20Architecture/Section%206%20-%20System%20Interrupts/Nested%20Interrupts.png)
### Summary
- Software allows a computer to execute different instructions without reconfiguring the hardware
- The meaning of the contents of [[Leeds University/Computer Science/Year 1/Computer Architecture/Section 9 - Memory/Definitions/Machine Word\|Machine Word]] of memory is defined by the context in which it is used
- It pays to set slow external processes to run concurrently but to keep interrupts to check their status
