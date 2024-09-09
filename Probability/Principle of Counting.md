Various methods of counting the number of ways an event can occur.

---
# Addition Principle
Also known as the rule of sum, is an intuitive idea that if we have $A$ number of ways of doing something and $B$ number of ways of doing another thing and we cannot do both at the same time, then there are $A+B$ ways to choose one of the actions.

Problem: Given 4 red marble, 3 blue marbles and 3 white marbles in a box. Randomly draw a ball from the box. How many ways are there to get a red **OR** blue marble?
Solution: 4 + 3 = 7 ways

![[AdditionPrinciple.png]]
Keyword: "or"

In set theory, if $S_1,S_2,\ldots,S_n$ are pairwise [[disjoint sets]] then we have:
$$
|S_1|+|S_2|+\cdots+|S_n| = |S_1\cup S_2\cup\cdots\cup S_n|
$$

---
# Multiplication Principle
Also known as the rule of product, is an intuitive idea that if we have $A$ number of ways of doing something and $B$ number of ways of doing another thing, then there are $A\cdot B$ ways of performing both actions.

Problem: Given 2 shirts and 2 shorts. Randomly select a shirt **AND** a short. How many ways are there to match the pair of clothing?
Solution: 2 x 2 = 4 ways
![[MultiplicationPrinciple.png]]
Keyword: "and"

In set theory, this multiplication principle is often taken to be the definition of the product of [[Cardinal Number]].
$$
|S_1|\times|S_2|\times\cdots\times|S_n| = |S_1\times S_2\times\cdots\times S_n|
$$
---
#Mathematics/Combinatorics
#CS30KMITL/Year1/Term1/ProbabilityStatistics