---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/year-2/algorithms-1/revision/sorting/"}
---

### Quick-Sort
```pseudo
\begin{algorithm}
\caption{Quick Sort}
\begin{algorithmic}
  \Procedure{quickSort}{$A, n$}
    \If{$n > 1$}
      \State pivot $\gets A[0]$
      \State Copy the elements of $A$ \textbf{smaller} than pivot to $S_1$
      \State Copy the elements of $A$ \textbf{equal} to pivot to $S_2$
      \State Copy the elements of $A$ \textbf{larger} than pivot to $S_3$
      \State \Call{quickSort}{$S_1, \text{length of } S_1$}
      \State \Call{quickSort}{$S_3, \text{length of } S_3$}
      \State Copy the elements back into $A$ in order $S_1, S_2, S_3$
    \EndIf
  \EndProcedure
\end{algorithmic}
\end{algorithm}
```
![Pasted image 20250115220034.png](/img/user/Leeds%20University/Computer%20Science/Year%202/Algorithms%201/Revision/images/Pasted%20image%2020250115220034.png)
Quick-sort has a time complexity of $O(n^{2})$, however this<ins> in the worst case</ins>
Quick-sort algorithm is important because of its <ins>average-case</ins> behaviour. It can be shown that the average number of comparisons made by quick-sort on a randomly generated array is proportional to $n\log_{2}n$
In practice, quick sort is usually faster than merge-sort. Besides, **in-place** implementation of quick-sort does not require additional memory
