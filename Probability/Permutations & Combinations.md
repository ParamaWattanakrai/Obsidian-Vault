# Permutations
Are **ORDERED** arrangement of $r$ objects from $n$ objects.
## Linear Permutations
With replacement: $n^r$
Without replacement:
- If $r\neq n$ then
$$
\begin{flalign}
_nP_r=P_{n,r}=\frac{n!}{(n-r)!}&&
\end{flalign}
$$
$$
\begin{flalign}
P(n;n_1,n_2,\ldots,n_k)=\frac{n!}{n_1!n_2!\cdots n_k!}&&
\end{flalign}
$$
- If $r=n$ then
$$
\begin{flalign}
P=n!&&
\end{flalign}
$$
## Circular Permutations
Without replacement:
- If $r\neq n$ then
$$
\begin{flalign}
\frac{_nP_r}{r}=\frac{n!}{(n-r)!r}&&
\end{flalign}
$$
- If $r=n$ then
$$
\begin{flalign}
(n-1)!&&
\end{flalign}
$$
With replacement: $(n-1)^r+r$ (Self-discovered, unlikely to be on the exam.)

---
# Combinations
Are **UNORDERED** arrangement of $r$ objects from $n$ objects.
- If $r\neq n$ then
$$
\begin{flalign}
_nC_r=C_{n,r}=\binom{n}{r}=\frac{_nP_r}{r!}=\frac{n!}{(n-r)!r!}&&
\end{flalign}
$$
## k Partitions
$n$ different items are partitioned into $k$ sections 
$$
\begin{flalign}
\binom{n_1}{r_1}\binom{n_2}{r_2}\cdots\binom{n_k}{r_k}&&
\end{flalign}
$$
![[kPartitions.png]]
## k Groups
$n$ different items are classified into $k$ groups
- If $\sum_{i=1}^{m}n_{i}=n$ and $n_1\neq n_2\neq\cdots\neq n_k$
$$
\begin{flalign}
\binom{n}{n_1}\binom{n-n_1}{n_2}\cdots\binom{n_k}{n_k}=\frac{n!}{n_1n_2\cdots n_k}&&
\end{flalign}
$$

#Mathematics/Combinatorics
#CS30KMITL/Year1/Term1/ProbabilityStatistics