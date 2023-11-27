---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/procedural-programming/double-pointers/"}
---

A double [[Leeds University/Computer Science/Compulsory Modules/Procedural Programming/Pointers\|pointer]] is simple a [[Leeds University/Computer Science/Compulsory Modules/Procedural Programming/Pointers\|pointer]] that points to another [[Leeds University/Computer Science/Compulsory Modules/Procedural Programming/Pointers\|pointer]]
	- This is useful for creating dynamic 2-d arrays
	- i.e. 2-d arrays where each array can have a different number of objects
{ #def}

This is done by [[Leeds University/Computer Science/Compulsory Modules/Procedural Programming/Dynamic Memory Allocation\|dynamically allocating memory ]]for an array of pointers, and each pointer in this array, points to a [[Leeds University/Computer Science/Compulsory Modules/Procedural Programming/Dynamic Memory Allocation\|dynamically allocated array]] of integers (or your desired data type)
```C title:Example
int **Matrix = (int **) malloc(sizeof(int*) * num_rows); // Creating the first dimension

for (int i = 0; i < num_rows; i++){
	Matrix[i] = (int *) malloc (sizeof(int) * num_col_per_row[i]);
} // Creating the second dimension
```
The first line creates a pointer to a dynamic array of pointers. ^[See [[Leeds University/Computer Science/Compulsory Modules/Procedural Programming/Pointers#The Definition of an Array\|Pointers#The Definition of an Array]]]
The pointers in this array are then allocated their own dynamic array of integers




