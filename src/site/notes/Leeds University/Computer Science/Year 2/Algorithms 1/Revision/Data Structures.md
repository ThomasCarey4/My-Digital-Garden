---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/algorithms-1/revision/data-structures/"}
---


recursion - 27

$$
\begin{align}
&\textbf{Abstract Data Type (ADT)}=
\begin{array}{l}
\text{Specification} \\
\text{of a }\textbf{data set}
\end{array}
+
\begin{array}{l}
\textbf{Operations} \\
\text{on that data}
\end{array}
\\ \\
&\textbf{Data Structure} =
\begin{array}{l}
\text{Implementation of an }\textbf{ADT}\text{ in a programming} \\
\text{language (OO languages – Classes)}
\end{array}
\end{align}
$$
### Lists
#### General Case
###### Operations
$$
\begin{aligned}
\begin{gather}
&\begin{array}{l}
\boxed{\text{Insert}} \\
\boxed{\text{Locate}} \\
\boxed{\text{Delete}} \\
\boxed{\text{Print}} \\
\end{array} \\
\textbf{Retrieve}
&\begin{cases}
\boxed{\text{Previous}} \\
\boxed{\text{Next}} \\
\boxed{\text{First}} \\
\boxed{\text{Last}}
\end{cases}
\end{gather} \\
\end{aligned}
$$

##### An Array Implementation of the **ADT** List
A **one-dimensional array** is a sequence of items of the same data type
- The items are stored contiguously in computer memory
- The items can be accessed by specifying their indices

- Each element occupies the same amount of computer storage
	- So changing the value won’t ever effect the other elements positions in memory
- As the position of each element in memory is constant and consistent, access time is $O(1)$
	- i.e. The address of $Item[k]=\text{The address of } Item[0] + k\times\text{The size of one item}$
An array should be instantiated of sufficient size $maxLength$, so that possible manipulations will keep the array within this limit:
$$
n\leq maxLength
$$
##### Insertion
**Insertion at the end**
- Requires $O(1)$ time as no other elements need to be changed
**Insertion at index anywhere else**
- Requires $O(n)$ time
	- Elements at locations $i,\ i+1,\ \dots,\ n-1$ have to be moved forward by 1
![Pasted image 20250115182704.png|500](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115182704.png)
##### Deletion
**Deletion at the end**
- Requires $O(1)$ time as no other elements need to be changed
**Deletion at index anywhere else**
- Requires $O(n)$ time
	- Elements at locations $i,\ i+1,\ \dots,\ n-1$ have to be moved back by 1
![Pasted image 20250115182815.png|500](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115182815.png)
##### A Linked Implementation of the **ADT** List
Linked lists are similar to arrays, however the data is *not* stored contiguously, instead each element contains the address of the next element in the list — where the last element contains *null* for the address
- Due to this, the size of each element can be different
![Pasted image 20250115184132.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115184132.png)
###### Insertion
Simply change the “Next” address inside the previous element: $O(1)$
- Will be $O(n)$ if the address of the predecessor is unknown
![Pasted image 20250115184217.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115184217.png)
###### Delete
Simply change the “Next” address inside the previous element: $O(1)$
- Will be $O(n)$ if the address of the predecessor is unknown
![Pasted image 20250115184411.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115184411.png)
###### Locate
Due to the nature of a linked list, you *must* use linear search, therefore: $O(n)$
![Pasted image 20250115184523.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115184523.png)

>[!warning] 
>Some operations become inefficient for linked lists.
>For example, printing a singly-linked list backwards requires $O(n^{2})$ time.

#### Stacks
A LIFO (Last-in-First-out) datatype
##### Operations
$$
\begin{aligned}
\begin{gather}
\boxed{\text{Push}} \\
\boxed{\text{Pop}}
\end{gather} \\
\end{aligned}
$$
- **Push**: Add to the **top** of the stack
- **Pop**: Delete from the **top** of the stack
##### Implementation
###### Array-based
- Faster as only inserting/deleting at the end and therefore $O(1)$
- Also $O(1)$ for reading a specific element in the stack
- Limited to a maximum size
###### Linked-list
**Reverse**:
Where each element points to the previous element (instead of the next)
- As fast as array-based for insertion/deletion ($O(1)$)
- $O(n)$ for reading a specific element
- No maximum size
- More memory as each element has to contain the address for the previous, and the address of the head needs to be stored
	- Slightly less memory than standard as the address at the “bottom” of the stack does not need to be stored
**Standard**:
- Same speed as reverse for insertion/deletion ($O(1)$)
- $O(n)$ for reading a specific element
- No maximum size
- More memory as each element has to contain the address for the previous, and the address of the head needs to be stored and the address for the tail needs to be stored
##### Uses
###### Reversing Strings
Due to the LIFO nature of stacks, simply “push”ing each character of the string to the stack (in order) and then “pop”ing them out will reverse the string.
###### Decimal → Binary
When converting from decimal to binary, the standard (and best) method prints the binary number in *reverse* and therefore has to be re-reversed.
**Wrong:**
![Pasted image 20250115201423.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115201423.png)
Stacks are particularly useful at this as, by their nature, they reverse the output of anything “pushed” into the stack (LIFO).
**Right:**
![Pasted image 20250115201416.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115201416.png)
###### Network/Graph Traversal
![Pasted image 20250115201720.png|600](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115201720.png)

#### Queues
**FIFO** (First-in-First-out)
A queue is a data structure which has a **front** end and a **rear** end and supports only two operations: **enqueue** and **dequeue**
- **Enqueue** — Add to the *rear* of the queue
- **Dequeue** — Delete from the *front* of the queue
##### Implementation
###### Array 1
The first method is the most simple, to store the queue with $Q[0]$ as the **front** and $Q[n]$ as the **rear**.
With this,
- **Enqueue** — Has a complexity of $O(1)$ as the address of the end is known
- **Dequeue** — Has complexity $O(n)$ as each element has to move “up” to $Q[0]$
![Pasted image 20250115204355.png|400](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115204355.png)
###### Array 2
Unlike the first method, this implementation allows $Q[0]$ to “drift” (i.e. change its address).
By allowing this, you no longer need to move all the other elements “up” the list when you **dequeue** (making **dequeue** $O(1))$. However, as the **front** drifts, the queue gets smaller.
![Pasted image 20250115204611.png|400](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115204611.png)
To fix this, you make the queue a loop. i.e. When the rear reaches $maxLength$, move it back to $0$ (provided the *front* isn’t still $0$)
![Pasted image 20250115204742.png|400](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115204742.png)
###### Linked List
With a linked there is no longer a $maxLength$, due to the data not being contiguous.
By only storing the address of the *front* and the address of the *rear*, you can have an infinitely long (as long as memory permits lol) queue by with both **enqueue** and **dequeue** having a complexity of $O(1)$
The only downsides of a linked list are the increased size of each element, due to storing the next address.
#### Priority Queues
A priority queue is similar to queue, however the two main operations are instead:
- **Insert**
- **Delete** — the element with the ***largest*** priority
##### Heaps
A heap is a partially-ordered binary tree, where (in a max-heap) the parent is always greater than the child, but the order of the children does not matter. Each parent in a heap **must** have two children, *unless* the children are on the last row — where they are pushed left.
![Pasted image 20250115211619.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115211619.png)
This can be stored as an array by artificially segmenting the array into "rows" of the heap:
$$
\boxed{42}
\ \vert\ 
\boxed{36}
\boxed{32}
\ \vert\ 
\boxed{16}
\boxed{12}
\boxed{30}
\boxed{20}
\ \vert\ 
\boxed{13}
\boxed{15}
\boxed{10}
$$
The depth ${\color{blue} d}$ of a heap with ${\color{red} n}$ elements is $\lfloor\log_{2}{\color{red} n}\rfloor$

###### Insertion $O(\log n)$
When adding an element to a heap:
1. Attach a new node with key ${\color{lightgreen} K}$ after the last leaf of the existing heap (the end of the array)
2. Sift ${\color{lightgreen} K}$ up to its appropriate place in the new heap (reverse bubble sort for just ${\color{lightgreen} K}$, and its parents):
	1. Compare ${\color{lightgreen} K}$ with its parent’s key
	2. If the parent’s key is greater than or equal to ${\color{lightgreen} K}$, stop
	3. Otherwise, swap these these two keys and repeat Step 2
###### Deletion (of the root) $O(\log n)$
When removing the root element of a heap:
1. Swap the root;s key with the last key ${\color{lightgreen} K}$ of the heap
2. Decrease the heap’s size by 1
3. Sift ${\color{lightgreen} K}$ down to its appropriate place in the new heap (bubble sort for just ${\color{lightgreen} K}$, and its parents):
	1. Compare ${\color{lightgreen} K}$ with the two keys of its children
	2. If ${\color{lightgreen} K}$ is not less than the two keys of its children, stop
	3. Otherwise, swap ${\color{lightgreen} K}$ with the largest of its children and repeat Step 3
###### Heap-Sort (Straightforward) $O(n\log n)$
**Phase 1**: Given an array ${\color{blue} A}$ of ${\color{red} n}$ elements, start with an initially empty heap and insert ${\color{blue} n}$ elements into the heap, one by one
**Phase 2:** Extract the elements from the heap in non-increasing order, putting them back into array ${\color{blue} A}$ in order (Just keep extracting(deleting) the root element)
###### Heap-Sort (Faster Phase 1) $O(n\log n)$
By improving the way we perform **Phase 1**, we can reduce its time complexity to $O(n)$. Due to **Phase 2** the overall complexity is still $O(n\log n)$ however it is undoubtedly faster than the straightforward method.
**The bottom-up algorithm**:
>[!check] 
>All ${\color{red} n}$ values are available at the beginning of the sort process (and the number of ${\color{red} n}$ values)

Basically, this algorithm works by calculating the depth of the resulting Heap ($\lfloor\log_{2}{\color{red} n}\rfloor$) and then filling the last row with the first ${\color{lightgreen} k}$ elements of the array:
![Pasted image 20250115215026.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115215026.png)
Next, you fill the row above:
![Pasted image 20250115215211.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115215211.png)
And sort it, to match the rules of a Heap:
![Pasted image 20250115215238.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115215238.png)
And voila!
Simply repeat this for the rest of the rows!

The complexity of this algorithm corresponds to the number of “sift-down” operations (coloured arcs)
For a complete binary tree, the total number of arcs is always less than $2n$
Hence $O(n)$ for Phase 1!

