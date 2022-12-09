---
aliases: ["COOK'S THEOREM","cook's theorem","Cook's Theorem"] 
---
Topics: #computerscience #finiteautomata #computabilitytheory 

## Cook's Theorem
$SAT \in$ [[class of NPC|NPC]].

### The Satisfiability Problem (SAT)
Given a boolean formula $\phi$ in $CNF$ with variables $x_1, x_2, \dots, x_n$ and clauses $c_1, \dots, c_m$, is $\phi$ satisfiable? In other words, is there a truth assignment $A$ to $x_1, \dots, x_n$ such that $\phi$ is true? 

The language of $SAT$ is as follows: $L_{SAT} = \{\langle \phi \rangle\ |\ \exists A$ that satisfies $\phi\}$.

Example of an instance for $SAT$:
- Variables: $x_1, x_2, x_3, x_4$
- Literals: Any variables and their negations, such as $x_1$ and $\bar{x_3}$. 
- Clauses: $c_1 =x_1∨ \bar{x_2} ∨x_3$, $c_2 =x_1∨x_2$, $c_3 = \bar{x_1} ∨x_2∨ \bar{x_3}∨ x_4$.
- Function/formula: $\phi = c_1∧c_2∧c_3$ The instance $\phi$ is $T$ by assignment $x_1 =T$, $x_2 =x_3 =x_4 =F$. Note: Many assignments satisfy $\phi$, but we only need one.

### Proof
From the definition of NPC, we need to prove that $SAT \in$ [[class of NP|NP]] and $\forall \Pi \in NP$, $\Pi \leq_p SAT$. 

To prove that $SAT \in NP$, we construct such a [[Nondeterministic Turing Machine|NTM]]:
NTM $N=$"On input $\langle \phi \rangle$ in $CNF$,
- Guess a truth assignment $A$   $O(n)$
- Verify if $\phi = T$ under $A$     $O(n+m)$
- If $T$, **accept**; else **reject**" 
Since $SAT$ is solvable by a nondeterministic Turing machine in polynomial time, it must be in $NP$. 

To prove that $\forall \Pi \in NP$, $\Pi \leq_p SAT$, we show that for any polynomial time NTM $M$, $L(M) \leq_p L_{SAT}$. 
