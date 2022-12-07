---
aliases: ["GRAPH COLORING PROBLEM","graph coloring problem","Graph Coloring Problem","GC"] 
---
Topics: #computerscience #finiteautomata #complexitytheory 

## Graph Coloring Problem (GC)

### Definition
Given graph $G = (V,E)$ and bound $B\geq 0$, is there a coloring scheme of the nodes that uses no more than $B$ colors such that no two nodes connected by an edge are given the same color?

### Solution
We define the following [[Nondeterministic Turing Machine|NTM]] $N$ to solve the graph coloring problem in polynomial time:

NTM $N$ =”On input $\langle G,B\rangle$,
1. Guess a coloring scheme (in polynomial time) $c : V\rightarrow C$
2. Verify if $|C|\leq B$ and $\forall(u,v)\in E,\ c(u) \neq c(v)$
3. if true, answer Yes; else answer No"

We have a nondeterministic algorithm (or [[Nondeterministic Turing Machine|NTM]]) that guesses a coloring scheme (or function) and verifies that for any $(u,v) \in E, c(u) \neq c(v)$ and that the number of colors used is no more than $B$, and further, all these can be done in polynomial time of $O(|V|) +O(|E|)$. Therefore, GC is in [[class of NP|NP]].
