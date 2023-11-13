---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-architecture/section-9-memory/definitions/dynamic-ram/","tags":["Definition"]}
---

**Dynamic [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/RAM\|RAM]] ( DRAM )**:
- Cells store bits as charge in capacitors
- Charge can leak so the cells need the periodically refreshed, even when powered ( hence **dynamic** )
- 100ms [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/Access Time\|latency]]
- Cheaper than [[Leeds University/Computer Science/Compulsory Modules/Computer Architecture/Section 9 - Memory/Definitions/Static RAM\|SRAM]] as capacitor is cheaper than transistor
### Refreshing
All DRAM requires a **refresh** operation
- A refresh circuit is included on the chip
- It disables the whole chip while refreshing
- It loops through the row, reading and then writing back the contents of each cell
64ms in standard
32ms in high
