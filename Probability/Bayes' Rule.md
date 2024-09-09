Is an extended application of [[Conditional Probability]]. Founded by Thomas Bayes. It is used to find $P(A|B)$ when we have $P(B|A)$.
$$
\begin{flalign}
P(A|B) = \frac{P(A\cap B)}{P(B)}\neq P(B|A)=\frac{P(B\cap A)}{P(A)}&&
\end{flalign}
$$
And since $P(A\cap B)=P(B\cap A)$, we get:
$$
\begin{flalign}
P(B\cap A)=P(B|A)P(A)&&
\end{flalign}
$$

Finally, we can substitute $P(B\cap A)$ into our first equation:
$$
\begin{flalign}
P(A|B)=\frac{P(B|A)P(A)}{P(B)}&&
\end{flalign}
$$
This is Bayes' Rule.

Usually, we need the [[Law of Total Probability]] to get $P(B)$.

#Mathematics/Probability
#CS30KMITL/Year1/Term1/ProbabilityStatistics