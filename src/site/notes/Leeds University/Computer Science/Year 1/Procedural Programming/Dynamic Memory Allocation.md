---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-1/procedural-programming/dynamic-memory-allocation/"}
---

Unlike higher level program languages ( Like Python ), C does not normally allow you to change the size of a data structure (e.g. an array) after it has been defined
- Dynamic Memory Allocation allows you to avoid memory waste by allocating exactly the memory required
{ #def}

```C
int *vector = (int *) malloc (sizeof(int)*array_size)
```
- Malloc ( $\color{blue} k$ ): allocate $\color{red}\text{at least}$ '$\color{blue} k$' bytes of memory
- $k$: `{C}'sizeof (int) * array_size'` is the size of the array in bytes
- Malloc returns a void type [[Leeds University/Computer Science/Year 1/Procedural Programming/Pointers\|pointer]]
	- `{C}'(int *)'` typecasts this to `{C}'int'`
