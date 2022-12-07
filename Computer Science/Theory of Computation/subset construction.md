---
aliases: ["SUBSET CONSTRUCTION","subset construction","Subset construction"] 
---
Topics: #computerscience #finiteautomata #automatatheory 

## Subset Construction
A method to convert [[Deterministic Finite Automaton|DFA]] to [[Nondeterministic Finite Automaton|NFA]]. 

### Definition
Given NFA $N=(Q,\Sigma,\delta,q_0,F)$, construct a DFA $M=N=(Q^{'},\Sigma,\delta^{'},q^{'}_0,F^{'})$ such that $L(M) = L(N)$. 
- Let $Q^{'} = 2^{Q}$, or the power set. $Q^{'}$ contains all subsets of $Q$. In the worst case, if $|Q|=n$, then $|Q^{'}| = 2^{n}$. In practice many states in $M$ could be inaccessible or dead-end states and are thrown away, so  $|Q^{'}| \leq 2^{n}$. 
- Let $q^{'}_0 = E(\{q_0\})$.
- Let $F^{'} = \{R \in Q^{'} | R \cap F \neq \emptyset \}$.
- For each $R \in Q^{'}$ and each $a \in \Sigma, \delta^{'}(R, a) = E(\cup_{p \in R} \delta(p, a))$.

