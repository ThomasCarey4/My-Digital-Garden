---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/operating-systems/revision/w1/p2-intro-to-operating-systems/"}
---


A **computer system** can be divided into four components:
- Hardware
- Operating System
- Application Programs
- User
>[!info] OS is a resource allocator
>Hardware (CPU, memory, mouse, keyboard, …) are resources. Multiple applications running on the system compete for them. The Operating System coordinates hardware use among Users and Applications.

![Pasted image 20250118165159.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Operating%20Systems/Revision/images/Pasted%20image%2020250118165159.png)

**User View**:
- Laptop or PC that consists of a monitor, keyboard, mouse, etc
- One user that wants to use all of the resources
- OS designed for **ease of use** rather than **resource utilisation**
- Many users interact with mobile devices: touch screen, voice recognition
>[!abstract] Embedded Systems
>Some computers have little or no use view: home appliances, various devices in cars, and other specialised computers that almost work in on their own

**System View**:
- Resource allocator, involved with hardware intimately
- Manages CPU time, memory space, storage space and I/O access
- Faces several requests—has to decide who gets the resources and who waits (users, applications)
- Responsible for overall efficient operations of the system
>[!abstract] Control Program
>Different view of OS. Manages the control of programs to prevent errors and improper use of the hardware

>[!tldr] Operating System
>- A **Kernel** (always running)
>- **Middleware** frameworks that allow development of applications
>- **System Programs** that aid in various OS tasks

