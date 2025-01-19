---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w2-os-services/p3-code-compilation-and-loading/"}
---


### Linkers and Loaders
Usually a program resides on a disk as a **binary executable file**. To run it, the executable has to be copied to memory and placed in the context of some process.
- **Relocatable object file**: source code compiled into object files suitable to be moved into a particular memory locations
- The **linker** combines these objects into a **binary executable**
- The **linker** may include standard libraries, such as ```math.h``` in C
- A **loader** loads the executable into memory to be run on the CPU
- **Relocation** assigns the final addresses to various parts of the executable after it is placed in memory
![Pasted image 20250119182805.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250119182805.png)
Consider running ```./main``` on the command line
1. The shell first creates a new process using the```fork()``` *system call*
2. The shell then invokes the **loader** with ```exec()```, passing it the name of the executable ```main```
3. The **loader** loads the program into main memory using the **address space of the new process**
A similar process occurs in a GUI by double clicking the executable with the mouse
#### Dynamic Linking
>[!tldr] tldr
>Dynamic Linking is when necessary libraries are linked dynamically when the program is being loaded into memory. This avoids linking and loading libraries that will not end up being used in the program. Instead, the library is loaded when, and if, it is required during run time. Possible memory space improvements.

#### ELF Format
Object files and executables typically have a standard format. It holds machine code and various metadata about the functions and variables in the program. Unix and Linux use the ELF format.
```bash
$ file PollutantApp
PollutantApp: ELF 64-bit LSB executable, ...
```
One data point of interest is the **entry point**—the address of the instruction to execute upon the start of the program
#### Why Applications are OS Specific
Applications compiled for one system (OS-hardware combination) usually will not work on a different system
- Each OS has unique system calls
- Possible solutions:
	- Use interpreted languages like Python, Ruby: interpreter on each system goes through the source code and executes the correct instructions and system calls. Interpreters can be limited
	- Use a language like Java that run on a VM
	- Compile code (such as C) for every different configuration
		- **Cross-Compiling**: Compile code on one system, for a different system
