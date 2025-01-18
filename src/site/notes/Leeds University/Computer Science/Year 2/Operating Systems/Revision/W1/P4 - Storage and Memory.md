---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w1/p4-storage-and-memory/"}
---


### Storage Structure
- The CPU can only load instructions from memory
	- Programs therefore must be loaded into memory to run
- Usually, programs are loaded to **RAM**
- Computers use other memory as well, Since **RAM** is volatile we cannot trust it to hold, for example, the **bootstrap program**, which runs on power on
- Read-only **EEPROM** (Electrically Erasable Programmable Read-Only Memory) memory—slow and rarely changed memory that preserves contents on power off
- Iphones, for example, use **EEPROM** to store serial numbers and other hardware information
#### Reminder of Units
A **bit** is a basic unit of storage. A **byte** is 8 bits
A **word** is one or more bytes, it varies between computer architectures. Register width and instruction size usually constitutes how large is a word.
$$
\text{Kilobytes, Megabytes, Gigabytes, Terabytes, Petabytes, ...}
$$
Or in fact, correct International Organisation for Standardisation (ISO) binary prefixed adopted in 2008 are:
$$
\text{Kibibytes, Mebibytes, Gibibytes, Tebibytes, Pebibytes, ...}
$$
$2^{10},2^{20},2^{30},...\text{ bytes}$

Memory is laid out in arrays of **bytes**, which have **addresses**
- The CPU interacts with memory by **load** and **store** instructions addressing specific bytes or words
- Bytes or words are moved between the CPU registers and the memory
- Similarly, the CPU loads instructions from the memory automatically, addressed by the **program counter**

**Von-Neumann Architecture**
- The **Instruction-Execution Cycle**: Fetch, Decode, Execute
- First, the CPU fetches an instruction from a program in memory, to an **instruction register**
- Then it decodes the instruction and executes it in the hardware
- The result *may* be stored back in memory
>[!abstract] Main Memory
>Ideally we would like the programs and data to be in fast **RAM** memory. This is not possible due to the **volatility** of the memory and relatively small size
>
#### Secondary Storage
Data is stored in secondary storage, which preserves programs and data while the system is off/
- Hard-disk drives (HDD)
- Nonvolatile memory (NVM) devices (M.2 drives)
>[!example] Other Storage
>CDs, cache, Blu-ray disk, magnetic tapes, …

#### Hierarchy
![Pasted image 20250118190329.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250118190329.png)
Operating systems have to balance all of these storage types for the whole system to work efficiently and reliably
#### I/O Structure
Interrupt driven memory access if fine for small requests, but moving a lot of data will not work very well.
**Direct Memory Access (DMA)** is used to offload work from the CPU.
The *device controller* directly transfers data to and from the device and main memory, without holding the CPU while doing so.
One interrupt is generated per transfer, to tell the device driver that the operation has completed. Better than to interrupt for every byte.
![Pasted image 20250118191006.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250118191006.png)
