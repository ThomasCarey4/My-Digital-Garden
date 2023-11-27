---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/procedural-programming/procedural-programming/","tags":["Mandatory-Module"]}
---


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/compulsory-modules/procedural-programming/pointers/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




Pointers are variables that store memory addresses
	- Typically of other variables

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
// Where x = Pointer to first item
// and y = how many steps after
```
In the 'Example 2', the variable 'array' is *effectively* a pointer to 'array\[0]'
When you call 'array\[1]' the program first points to 'array\[0]' and then *steps* to next memory address, which would be 'array\[1]'


</div></div>

