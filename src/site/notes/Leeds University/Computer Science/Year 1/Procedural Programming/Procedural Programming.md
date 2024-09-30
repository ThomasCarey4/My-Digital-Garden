---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/procedural-programming/procedural-programming/","tags":["Mandatory-Module"]}
---

#### Pointers

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/procedural-programming/pointers/#def" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



Pointers are variables that store memory addresses
	- Typically of other variables 

</div></div>

#### Dynamic Memory

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/procedural-programming/dynamic-memory-allocation/#def" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



- Dynamic Memory Allocation allows you to avoid memory waste by allocating exactly the memory required 

</div></div>

#### Double Pointers

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/leeds-university/computer-science/year-1/procedural-programming/double-pointers/#def" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




A double [[Leeds University/Computer Science/Year 1/Procedural Programming/Pointers\|pointer]] is simple a [[Leeds University/Computer Science/Year 1/Procedural Programming/Pointers\|pointer]] that points to another [[Leeds University/Computer Science/Year 1/Procedural Programming/Pointers\|pointer]]
	- This is useful for creating dynamic 2-d arrays
	- i.e. 2-d arrays where each array can have a different number of objects This is done by [[Leeds University/Computer Science/Year 1/Procedural Programming/Dynamic Memory Allocation\|dynamically allocating memory ]]for an array of pointers, and each pointer in this array, points to a [[Leeds University/Computer Science/Year 1/Procedural Programming/Dynamic Memory Allocation\|dynamically allocated array]] of integers (or your desired data type)
```C title:Example
int **Matrix = (int **) malloc(sizeof(int*) * num_rows); // Creating the first dimension

for (int i = 0; i < num_rows; i++){
	Matrix[i] = (int *) malloc (sizeof(int) * num_col_per_row[i]);
} // Creating the second dimension
```
The first line creates a pointer to a dynamic array of pointers. ^[See [[Leeds University/Computer Science/Year 1/Procedural Programming/Pointers#The Definition of an Array\|Pointers#The Definition of an Array]]]
The pointers in this array are then allocated their own dynamic array of integers






</div></div>

