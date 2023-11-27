---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/procedural-programming/pointers/"}
---

Pointers are variables that store memory addresses
	- Typically of other variables
{ #def}


This is useful for directly modifying a variable outside of your scope
```embed-c
PATH: "https://raw.githubusercontent.com/ThomasCarey4/COMP1711/main/pointers.c"
TITLE: "Example 1"
```
This code will directly modify the 'num' variable from inside the test function, **without** returning it or creating a copy.

This is useful because, for example, if 'num' was a *really* large data type (such as a massive array) you can modify it inside functions without taking the time to create a local copy of the variable.
- This allows for significant increases in spatial and temporal efficiency

###### Syntax
```C
&num // = The address of 'num'
*add // = The value stored at address 'add'
*&num // = The value at the address of 'num' = 'num'
%p // = The format specifier for a memory address
```
### Pointer Arithmetic
```embed-c
PATH: "https://raw.githubusercontent.com/ThomasCarey4/COMP1711/main/pointer-arithmetic.c"
TITLE: "Example 2"
```
The reason this works is because in C arrays are defined by:
```C
x[y]
// Where x = Pointer to the first item
// and y = how many steps after
```
In the 'Example 2', the variable 'array' is *effectively* a pointer to 'array\[0]'
When you call 'array\[1]' the program first points to 'array\[0]' and then *steps* to next memory address, which would be 'array\[1]'
###### Syntax
```C
*add++ // = Access the address, then add 1
*++add // = Add 1 to the address, then access it
```
