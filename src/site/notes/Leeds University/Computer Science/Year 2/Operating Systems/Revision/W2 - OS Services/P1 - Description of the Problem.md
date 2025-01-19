---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w2-os-services/p1-description-of-the-problem/"}
---


### Operating System Services
The set of features that are the most directly helpful to the user:
- **User Interface (UI)**: Graphical, touch-screen, command-line interface, …
- **Program Execution**: Load programs from memory and run them
- **I/O Operations**: Access data from files or I/O devices. For efficiency and protection, users cannot do so directly: OS services do that for us
- **File-System Manipulation**: Read, write, create, delete, search files. Access permission control
- **Communications**: Communicate between processes. **Shared memory** or **message passing** communications
- **Error Detection**: Errors occur in CPU, memory, I/O devices, user programs: OS has to detect, correct and report errors. Sometimes it may decide to halt the system

Other features are mainly for the operations of the system:
- **Resource Allocation**: Multiple processes are running on the system and they should be allocated resources: CPU cycles, main memory, file storage, I/O device access
- **Logging**: Keep track of which programs need/use what resources
- **Protection and Security**: Protect information between different users on the system. Make sure processes do not interfere. Control resource access. Security from the outside: control access to the system
### User and OS Interface
#### Command Interpreters
>[!info] Command Interpreters
>On UNIX and Linux systems there are multiple options: C Shell, Bourne-Again Shell (BASH), Korn Shell. The main function is to execute user supplied commands, which usually modify files on the system

The commands can be built into the shell or they can be a separately stored executable which the shell can invoke. The latter requires no modification to the shell when adding new commands.

#### Graphical User Interface
Instead of entering commands directly, we could use a **Graphical User Interface**—a mouse-based window-and-menu interface.

Users move mouse and click on images that represent files, executables, directories, to interact with them.

The first GUI appeared in 1973.

Apple made GUI (desktop) widespread in the 1980s.

On UNIX systems traditionally command line dominated, but open-source GUIs exist: KDE, GNOME, ...
**Touchscreen** is a form of GUI common on mobile devices.