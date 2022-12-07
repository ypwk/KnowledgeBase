---
aliases: ["NONDETERMINISTIC TURING MACHINE","nondeterministic turing machine","Nondeterministic Turing Machine","Nondeterministic Turing Machines","nondeterministic turing machines", "NTM"] 
---
Topics: #computerscience #finiteautomata #automatatheory 

## Nondeterministic Turing Machine

### Definition
A [[Nondeterministic Turing Machine]] is an unrealistic (unreasonable) model of computing which can be simulated by other models with an exponential loss of efficiency. It is a useful concept that has had great impact on the theory of computation.

NFA $N=(Q,\Sigma,\Gamma,\delta,q_0,q_{accept},q_{reject})$, where $\delta : Q \times \Gamma → 2^P$ for $P = Q\times\Gamma\times\{L,R\}$.

Given state $q$ and input $X$, $\delta(q,X)$ is a set a moves. How does the machine know which one to choose? This is nondeterminism. The computation can be illustrated by a tree, with each node representing a configuration.

Nondeterminism can be viewed as a kind of parallel computation wherein multiple independent processes or threads can be running concurrently. When a nondeterministic machine splits into several choices, that corresponds to a process forking into several children, each then proceeding separately. If at least one process accepts, then the entire computation accepts. 

### Time Complexity
Let $N$ be an nondeterministic Turing Machine that is a decider (where all computation paths halt in the tree for any input). The time complexity of $N$, $f(n)$, is the maximum number of steps that $N$ uses on any computation path for any input of length $n$. In other words, $f(n)$ is the maximum height of all computation trees for all input of length $n$.

### Alternative Definition
There are two phases for operation: 
- Guessing phase: Guess a solution (always on target). 
- Verifying phase: Verify the solution.

### Theorems
Every $T(n)$-time single-tape nondeterministic Turing Machine has an equivalent $O(2^{O(T(n))})$-time single-tape [[Deterministic Turing Machine]].