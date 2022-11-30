---
aliases: ["TRANSITION FUNCTION","transition function","Transition function","Transition functions","transition functions"] 
---
Topics: #computerscience #automatatheory #finiteautomata

## Transition Function ($\delta$)
$\delta : Q \times \Sigma \rightarrow Q$ is a transition function, where $\delta(q,a) = p$ is the state that $M$ will enter if the current state is $q$ and the current symbol is $a$, given $Q$ a finite set of states and $\Sigma$ an [[alphabet]]. 

## Extended Transition Function ($\hat{\delta}$)
Extending $\delta$ to $\hat{\delta} : Q \times \Sigma^* \rightarrow Q$: For any $q \in Q$ and any $w = xa \in \Sigma^*$ , define $\hat{\delta}(q,x)$ recursively as below:
- $\hat{\delta}(q,\epsilon) = q$
- $\hat{\delta}(q,w) = \delta(\hat{\delta}(q,x),a)$

Thus, this is the language recognized by a [[Deterministic Finite Automaton|DFA]] $M: L(M) = \{w\ |\ \hat{\delta}(q0,w)\in F\}$

