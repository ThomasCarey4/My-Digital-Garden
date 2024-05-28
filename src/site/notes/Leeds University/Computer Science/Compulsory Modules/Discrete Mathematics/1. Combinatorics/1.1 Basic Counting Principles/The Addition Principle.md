---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/discrete-mathematics/1-combinatorics/1-1-basic-counting-principles/the-addition-principle/"}
---

###### The Addition Principle for Counting Procedures
If a procedure can be broken up into ${\color{red} m}$ events or cases whose [[Leeds University/Computer Science/Compulsory Modules/Fundamental Math Concepts/5. Set Theory/5.1 Sets\|sets]] of outcomes are mutually exclusive, with ${\color{blue} j}_{1}$ possible outcomes for the first event, ${\color{blue} j}_{2}$ possible outcomes for the second event, $\dots$, and ${\color{blue} j}_{\color{red} m}$ for the ${\color{red} m}^{th}$ event, then the total number of outcomes of the procedure is ${\color{blue} j}_{1}+{\color{blue} j}_{2}+\dots+{\color{blue} j}_{{\color{red} m}}$
###### <hr>

>[!example] 
>On a bookshelf there are *5* different calculus books, *6* different linear algebra books and *7* different combinatorics books
>1. In how many ways can a pair of books of different types be chosen
>2. In how many ways can single book of each type be chosen

**Part 1:**
*Mutually Exclusive Events*:
- Calculus + Linear Algebra
	- $5\times6$ choices
- Calculus + Combinatorics
	- $5\times7$ choices
- Linear Algebra + Combinatorics
	- $6\times7$ choices
$\therefore$ Total number of outcomes $\coloneqq (5\times6)+(5\times7)+(6\times7)=107$
**Part 2:**
*Independent Events*:
- Calculus book
	- 5 choices
- Linear Algebra book
	- 6 choices
- Combinatorics book
	- 7 choices
$\therefore$ Total number of outcomes $\coloneqq 5\times6\times7=210$

>[!example] 
>How many integers are the from 1 through 9999 that have distinct digits?

**Answer**:
*Mutually Exclusive Events*:
- One digit
	- 9
- Two digits
	- $9\times(10-1)=9\times9$
	- First digit can’t be 0, second cant be the same as the first
- Three digits
	- $9\times9\times8$
- Four digits
	- $9\times9\times8\times7$
$\therefore$ Total number of integer $\coloneqq(9)+(9\times9)+(9\times9\times8)+(9\times9\times8\times7)=$
