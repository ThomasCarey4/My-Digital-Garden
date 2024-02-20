---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/computer-processors/hardware-description-language/"}
---

A HDL definition defines the internal wiring of a chip and consists of 2 parts
- A *header* section - defining the interface of the chip
- A *parts* section - defining the names and internal top

> [!tip] 
> - Each chip is defined in a seperate text file
> - A chip called Xxx is defined in a file called Xxx.hdl (case sensitive!!)
> - Keywords are capitalised
> - Identifier name may be sequence of letters and digits not starting with a digit
> - Whitespace has no meaning
> - Lines end with semicolons

#### Defining a Chip

```nand2tetris-hdl title="Xor.hdl (Filename is important)"
CHIP Xor {
   IN a, b;
   OUT out;

   PARTS:
   And (a=a, b=b, out=x);
   Or (a=a, b=b, out=y);
   Not (in=x, out=notx);
   And (a=y, b=notx, out=out);
}
```
These parts are like functions but each paramater is defined when calling it
- The order of the *parts* is **not** important
So a *Xor* gate takes 4 ‘functions’ to work
![Xor Gate.png](/img/user/Leeds%20University/Computer%20Science/Compulsory%20Modules/Computer%20Processors/images/Xor%20Gate.png)

#### Defining a Chip (Buses)
- Buses are a collection of pins
- Buses can be used as input, output or internal pins
- Buses are indexed (similar to arrays in C)
```nand2tetris-hdl title:"bus.hdl"
CHIP foo {
   IN in[8];
   OUT out[8];

   //Parts
}
```
