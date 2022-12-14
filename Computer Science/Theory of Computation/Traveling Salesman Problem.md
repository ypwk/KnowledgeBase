---
aliases: ["TRAVELING SALESMAN PROBLEM","traveling salesman problem","Traveling salesman problem","TSP","Traveling Salesman Problem"] 
---
Topics: #computerscience #finiteautomata #complexitytheory 

## Traveling Salesman Problem

### Definition
Given an edge-weighted graph $G(V,E,w)$ with a bound $B\geq0$, is there a tour (a cycle that passes through each node exactly once) in $G$ with total weight no more than $B$?

### Solution
We define the following [[Nondeterministic Turing Machine|NTM]] $N$ to solve the TSP in polynomial time:

NTM N =”On input $\langle G,B\rangle$ 
1. Nondeterministically guess a tour $T$ — runtime: $O(|V|)$
2. Verify if $T$ includes every node once — runtime: $O(|V|)$
3. Compute sum ← $\sum_{e\in T} w(e)$ — runtime: $O(|V|)$
4. Verify if sum $\leq B$. If true, answer Yes; else No" — runtime: $O(1)$ 

The time complexity of $N$ is $O(|V|)$. If the answer to the problem is ”Yes”, $N$ guarantees that the right $T$ will be guessed in step 1, because the acceptance of an input by a nondeterministic machine is determined by whether there is an accepting computation among all, possibly exponentially many, computations.

In the above proof, if there is a solution, i.e., a tour with total weight no more than B, it will always be generated by the Turing machine. This is like that a nondeterministic machine has a guessing power. A tour can only be found by a deterministic machine in exponential time, however, it can be found by a nondeterministic machine in just linear steps. Any nondeterministic proof should always contain two stages: Guessing and verifying.