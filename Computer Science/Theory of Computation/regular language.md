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

A common problem is a proof that a regular language is non-regular by closure property.  The following is a blueprint for such a proof: 
- To prove that regular language $A$ is non-regular, assume it is regular for the sake of contradiction. 
- Find a regular language $B$ and a language operator that preserves regularity, and then apply the operator on $A$ and $B$ to get a regular language $C$. 
- If $C$ is known to be non-regular, a contradiction is found, and $A$ must be non-regular. 

### Practice
1. [Closure Properties] Prove that $A=\{w \in \{a,b\}^{*}|$w is of odd length and contains an even number of a’s$\}$ is regular. 
	- Let $A_1 =\{w|w$ is of odd length$\}$ 
	- Let $A_2 =\{w|w$ has an even number of a’s$\}$ 
	- Since DFAs exist to accept $A_1$ and $A_2$, both are RLs. 
	- $A=A1 \cap A2$. By the CP of RLs under intersection, $A=A1 \cap A2$ is RL. So $A$ is RL.
2. [Closure Properties] Prove that $C=\{w \in{0,1}^{*}|w$ has an equal # of 0s and 1s$\}$ is **not regular**.
	- Assume for contradiction that $C$ is regular.
	- Let $B =\{0^{*}1^{*}\}$. B is a known regular language. 
	- Let $D =C \cap B=\{0^n1^n\}$. $D$ is known to be non-regular But $D$ is regular by closure properties under intersection.
	- A contradiction! So $C$ is non-regular.
3. [Closure Properties]
4.  