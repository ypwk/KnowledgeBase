---
aliases: ["POST'S CORRESPONDENCE PROBLEM","post's correspondence problem","Post's Correspondence Problem","PCP"] 
---
Topics: #computerscience #computabilitytheory #finiteautomata 

## Post's Correspondence Problem
How do we determine the computability of problems that aren't related to [[Turing Machine|Turing Machines]]?

Given the input $P=\{ \frac{t_1}{b_1}, \frac{t_2}{b_2}, \dots, \frac{t_k}{b_k}\}$, where $t_1, t_2, \dots, t_k$ and $b_1, b_2, \dots, b_k$ are strings over [[alphabet]] $\Sigma$, does $P$ contain a match? In other words, is there $i_1, i_2, \dots, i_n \in \{1,2,\dots,k\}$ with $n\geq1$ such that the concatentation of the tops and the bottoms, $t_{i_1}t_{i_2}\dots t_{i_n}$ and $b_{i_1}b_{i_2}\dots b_{i_n}$, are equal?

We can think of P as a collection of dominos, each containing two [[word|strings]], with one stacked on top of the other.

Defined as a [[language]], we have $L_{PCP}=\{\langle P\rangle|P$ is an instance of $PCP$ with a match$\}$.

For example, for input $P_1=\{\frac{b}{ca},\frac{a}{ab},\frac{ca}{a},\frac{abc}{c}\}$, the sequence $2, 1, 3, 2, 4$, or $\frac{a}{ab}\frac{b}{ca}\frac{ca}{a}\frac{a}{ab}\frac{abc}{c}$ is a match. For $P_2=\{\frac{abc}{ab},\frac{ca}{a},\frac{acc}{ba}\}$, there are no matches since all of the top strings are longer than the bottom strings. 

Post's Correspondence Problem is [[Turing Decidable Language|non-TD]] for the binary alphabet. However, Post's Correspondence Problem is [[Turing Decidable Language|TD]] for the unary alphabet. You can show that there exists a simple algorithm to solve the unary case.