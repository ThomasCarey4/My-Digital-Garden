---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/2-os-services/code-compilation-and-loading/"}
---


###### Linkers and Loaders
Usually a program resides on a disk as a **binary executable file**. To run it, the executable has to be copied to memory and placed in the context of some process.
- **Relocatable object file**: source code compiled into object files suitable to be moved into a particular memory location
- The **linker** combines these object into a **binary executable**
- The **linker** may include standard libraries, such as $math.h$ in C
- A **loader** loads the executable into memory to be run on the CPU
- **Relocation** assigns the final addresses to various parts of the executable after it is placed in memory
![Pasted image 20241010123804.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/2.%20OS%20Services/images/Pasted%20image%2020241010123804.png)
>[!info] 
>Consider running ```./main``` on the command line
>- The shell first creates a new process using the ```fork()``` system call
>- The shell then invokes the loader with ```exec()``` passing it the name of the executable: ```main```
>- The **loader** loads the program into main memory using the **address space of the new process**
>- A similar process occurs in the GUI by double clicking the executable with the mouse

#TODO Dynamic Linking

