---
aliases: ["REGULAR LANGUAGE","regular language","Regular language","Regular languages","regular languages", "RL", "rl", "RLs"] 
---
Topics: #computerscience #automatatheory #finiteautomata

## Regular Language (RL)
A [[language]] is called a regular language if some [[Deterministic Finite Automaton|DFA]] or [[Nondeterministic Finite Automaton|NFA]] accepts it. 

### Theorem
DFA, NFA, and regular languages have the same computational power.

### Closure Properties
- Union: 
	- If $A$ and $B$ are regular, so is $A \cup B$. 
- Concatenation: 
	- If $A$ and $B$ are regular, so is $AB$. 
	- Thus, if $A$ is regular, it is also closed under power. 
- Kleene Star:
	- If $A$ is regular, so is $A^{*}$.
- Intersection
	- If $A$ and $B$ are regular, so is $A \cap B$. 
- Complement
	- If $A$ is regular, so is $\bar{A}=\Sigma^{*}-A$.
- Difference
	-  If $A$ and $B$ are regular, so is $A-B = A \cap \bar{B}$. 
- Reverse
	- If $A$ is regular, so is $A^{R}$.
- Homomorphism
	- If $A$ is regular, so is $h(A)=\{h(w)|w \in A\}$ for a homomorphism $h : \Sigma \rightarrow (\Sigma^{'})^{*}$.
- Inverse Homormorphism
	- If $A$ is regular, so is $h^{-1}(A)=\{w|h(w) \in A\}$ for a homomorphism $h : \Sigma \rightarrow (\Sigma^{'})^{*}$.

### Practice
1. Prove that $A=\{w \in \{a,b\}^{*}|$w is of odd length and contains an even number of a’s$\}$ is regular. 
	- Let $A_1 =\{w|w$ is of odd length$\}$ 
	- Let $A_2 =\{w|w$ has an even number of a’s$\}$ 
	- Since DFAs exist to accept $A_1$ and $A_2$, both are RLs. 
	- $A=A1 \cap A2$. By the CP of RLs under intersection, $A=A1 \cap A2$ is RL. So $A$ is RL