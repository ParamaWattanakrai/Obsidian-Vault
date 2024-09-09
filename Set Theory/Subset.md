A set is a subset of another set if all of its elements are also elements of another set.
A set $A$ is a subset of a set $B$ if all elements of $A$ are also elements of $B$; $B$ is then a superset of $A$.
$$
\begin{flalign}
A\subseteq B&&
\end{flalign}
$$
"A is a subset of B"

Which can also be quantified as: $\forall x(x\in A \to x\in B)$

Example:
$A=\{1,2,3,4,5\}$
4 is not a subset of $A$ because 4 is not a set

---
# Properties
|              | Subset $\subseteq$                                 |               | Proper Subset $\subsetneq$ or $\subset$               |
| ------------ | -------------------------------------------------- | ------------- | ----------------------------------------------------- |
| Reflexivity  | Given any set $A$, $A\subseteq A$                  | Irreflexivity | Given any set $A$, $A\subsetneq A\equiv F$            |
| Transitivity | $A\subseteq B \land B\subseteq C \to A\subseteq C$ | Transitivity  | $A\subsetneq B \land B\subsetneq C \to A\subsetneq C$ |
| Antisymmetry | $A\subseteq B\land B\subseteq A\to A = B$          | Asymmetry     | $A\subsetneq B\to B\subsetneq A\equiv F$              |

---
# Proper Subset
Also known as strict subset.
If $A\subseteq B$ but $A\neq B$, then A is a proper subset of $B$
$$
\begin{flalign}
A\subset B \text{ or } A\subsetneq B&&
\end{flalign}
$$
It also means that $|A|<|B|$