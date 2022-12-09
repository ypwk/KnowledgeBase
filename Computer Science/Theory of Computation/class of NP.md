---
aliases: ["CLASS OF NP","class of np","Class of NP","NP","NP-hard"] 
---
Topics: #computerscience #finiteautomata #complexitytheory 

## Class of NP

### Definition
NP is the class of problems solvable in polynomial time by [[Nondeterministic Turing Machine|nondeterministic turing machines]], or in exponential time by [[Deterministic Turing Machine|deterministic turing machines]].

To prove that a problem $\Pi \in NP$, design a polynomial-time nondeterministic algorithm with two steps, **guess** and **verify**. 

### Theorems
Any problem $\Pi \in NP$ can be solved using a [[Deterministic Turing Machine]] in time $O(c^{p(n)})$ for some $c > 0$ and polynomial $p(n)$.