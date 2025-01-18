---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w1/p3-concept-of-interrupts/"}
---


### Computer-System Organisation
![Pasted image 20250118171148.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250118171148.png)
- Many devices competing for memory access
- OS uses **device drivers** to talk to various controllers
- Memory has a **memory controller** which also does some managing to keep up with many reads and writes at once
$$\boxed{\text{We now go deeper into various concepts within this system!}}$$
### Interrupts
Consider a serious of events within the system when we press a key on a keyboard. This constitutes input/output (I/O)
1. Device driver writes to appropriate registers (memory locations) in the device controller
2. The controller reads to see what needs to be done (e.g. read a character from the keyboard)
3. Controller starts transfer of data from the keyboard
4. Controller informs the driver that a transfer has been done
5. Driver gives control to OS, to read the data
How does the controller inform the driver (CPU) that is has finished an operation? Though an **interrupt**!

<hr>

- Hardware may trigger interrupts at any time
- The CPU then stops what it is doing and checks if it can service the interrupt, through the **interrupts service routine**
- When serviced, the CPU goes back to what it was doing

- The CPU may need to store the current **program counter**, for example into the **link register** or **stack**—to get back to what is was doing before the interrupt
- The interrupt routine has to save any CPU state that it will be changing, and return it back to what it was once finished
- Once done, the program counter and the original program execution continue

<hr>

Requirements for an effective interrupt system:
- The capability to defer interrupts when something more important is being done on the CPU
- An efficient way to service interrupts—can’t take too long to respond
- A structure for **high and low priority interrupts**

#### Advanced Material
- When an interrupt occurs, the correct interrupt service routine needs to be discovered
- There can be hundreds to search through, but we need to be fast
- Instead of searching, a table of pointers to interrupt service routines can be used: **interrupt vector**
- A unique ID on interrupts is indexing this vector, which sends CPU straight to the correct interrupt service routine
In reality, the vectors get too big and a hybrid approach is used, **interrupt chaining**
- Interrupt routines point to the next interrupt routine, we loop through them until the right one is found
	- Circularly Looped Linked List??
- **Nonmaskable interrupts**: unrecoverable errors, such as memory read/write faults
- **Maskable interrupts**: the CPU can turn these off before starting some critical code section
#### Advanced Terms
***Raise an Interrupt***: Ask the CPU to stop what it is doing and do something for me
***Catch an Interrupt***: the CPU discovers someone wants processing time
***Dispatch the Interrupt***: Call an *interrupt handler*
***Clear the Interrupt***: Call the correct interrupt service routine

