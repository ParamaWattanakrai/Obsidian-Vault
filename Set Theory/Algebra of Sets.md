Defines the properties and law of sets.

# Set Operations
Are operations that are applied on two or more sets to develop a relationship between them and create a new set.
## Summary
Let $U=\{1,2,3,4,5,6,7,8,9,10\}$, $A=\{1,2,3\}$ and $B=\{3,4,5\}$

|                      | Expression               | Quantifier                                                                       | Result                                                      |
| -------------------- | ------------------------ | -------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| Union                | $A\cup B$                | $\{x\|x\in A\text{ or } x\in B\}$                                                | $\{1,2,3,4,5\}$                                             |
| Intersection         | $A\cap B$                | $\{x\|x\in A\text{ and } x\in B\}$                                               | $\{3\}$                                                     |
| Complement           | $A'$ or $A^c$            | $\{x\in U\|x\notin A\}$                                                          | $\{4,5,6,7,8,9,10\}$                                        |
| Difference           | $A-B$ or $A\backslash B$ | $\{x\|x\in A\text{ and } x\notin B\}$                                            | $\{1,2\}$                                                   |
| Symmetric Difference | $A\Delta B$              | $\{x\|(x\in A\text{ and } x\notin B)\text{ or }(x\in B\text{ and } x\notin A)\}$ | $\{1,2,4,5\}$                                               |
| Cartesian Product    | $A\times B$              | $\{(x,y)\|x\in A\text{ and } y\in B\}$                                           | $\{(1,3),(1,4),(1,5),(2,3),(2,4),(2,5),(3,3),(3,4),(3,5)\}$ |

---
## Union
$$
\begin{flalign}
A\cup B=\{x|x\in A\text{ or } x\in B\}&&
\end{flalign}
$$

Cardinal Formula: $|A\cup B|=(|A|+|B|)-|A\cap B|$
## Intersection
$$
\begin{flalign}
A\cap B=\{x|x\in A\text{ or } x\in B\}&&
\end{flalign}
$$

Cardinal Formula: $|A\cap B|=(|A|+|B|)-|A\cup B|$
## Complement
$$
\begin{flalign}
A'=\{x\in U|x\notin A\}&&
\end{flalign}
$$
Also notated as: $A^c$
Cardinal Formula: $|A'|=|U|-|A|$
## Difference
$$
\begin{flalign}
A-B=\{x|x\in A\text{ and } x\notin B\}&&
\end{flalign}
$$
Also notated as: $A\backslash B$
Also known as relative complement: $A-B=A\cap B'$

Cardinal Formula: $|A-B|=|A|-|A\cap B|$
## Symmetric Difference
$$
\begin{flalign}
A\Delta B=\{x|(x\in A\text{ and } x\notin B)\text{ or }(x\in B\text{ and } x\notin A)\}&&
\end{flalign}
$$
$A\Delta B=(A\cup B)-(A\cap B)=(A-B)\cup(B-A)$

Cardinal Formula: $|A\Delta B|=|A\cup B|-|A\cap B|$
## Cartesian Product
$$
\begin{flalign}
A\times B=\{(x,y)|x\in A\text{ and } y\in B\}&&
\end{flalign}
$$

---
# Properties and Laws
## Fundamental Properties

|              | Commutative       | Associative                      |
| ------------ | ----------------- | -------------------------------- |
| Union        | $A\cup B=B\cup A$ | $(A\cup B)\cup C=B\cup(A\cup C)$ |
| Intersection | $A\cap B=B\cap A$ | $(A\cap B)\cap C=B\cap(A\cap C)$ |

|                         | Distributive                            |
| ----------------------- | --------------------------------------- |
| Union over intersection | $A\cup(B\cap C)=(A\cup B)\cap(B\cup C)$ |
| Intersection over union | $A\cap(B\cup C)=(A\cap B)\cup(B\cap C)$ |

|              | Identity               | Complement           |
| ------------ | ---------------------- | -------------------- |
| Union        | $A\cup\emptyset=A$<br> | $A\cup A'=U$         |
| Intersection | $A\cap U=A$            | $A\cap A'=\emptyset$ |

---
## Additional Laws
### Union and Intersection

|              | Idempotent      | Domination                  | Absorption         |
| ------------ | --------------- | --------------------------- | ------------------ |
| Union        | $A\cup A=A$<br> | $A\cup U=U$                 | $A\cup(A\cap B)=A$ |
| Intersection | $A\cap A=A$     | $A\cap \emptyset=\emptyset$ | $A\cap(A\cup B)=A$ |
### Complement
|              | De Morgan's                |
| ------------ | -------------------------- |
| Union        | $(A\cup B)'=A'\cap B'$<br> |
| Intersection | $(A\cap B)'=A'\cup B'$     |

|         | Double Complement (Involution) |
| ------- | ------------------------------ |
| Any Set | $(A')'=A$<br>                  |

|               | For Universal Set and Empty Set |
| ------------- | ------------------------------- |
| Universal Set | $\emptyset'=U$<br>              |
| Empty Set     | $U'=\emptyset$                  |

---
## Principle of Duality
Asserts that for any true statement about sets, the dual statement obtained by interchanging unions and intersections, interchanging $U$ and ⁠$\emptyset$ and reversing inclusions is also true. A statement is said to be self-dual if it is equal to its own dual.

---