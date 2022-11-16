---
aliases: ["DETERMINISTIC FINITE AUTOMATON","deterministic finite automaton","Deterministic Finite Automaton","Deterministic Finite Automata","deterministic finite automata","DFA"] 
---
Topics: #computerscience #automatatheory #finiteautomata

## Deterministic Finite Automaton (DFA)

### Definition
DFA $M=(Q,\Sigma,\delta,q_0,F)$, where 
- $Q$ is a finite set of states
- $\Sigma$ is an [[alphabet]]
- $q_0\in Q$ is a start state
- $F\subseteq Q$ is a set of accept/final states
- $\delta : Q \times \Sigma \rightarrow Q$ is a [[transition function]], where $\delta(q,a) = p$ is the state that $M$ will enter if the current state is $q$ and the current symbol is $a$.

Thus, this is the language recognized by a [[Deterministic Finite Automaton|DFA]] $M: L(M) = \{w\ |\ \hat{\delta}(q0,w)\in F\}$, where $\hat{\delta}$ is an extended [[transition function]].

### Components
- A tape of squares, with the same length of the input string 
- A control unit that keeps track of the current state and follows the $\delta$ function 
- The head that reads and moves to the right, one square at a time 
- The DFA accepts the input string if the head reaches the end of the tape and the control unit sees the final state

A DFA accepts a string if there exists a path in the diagram that starts from $q_0$ and ends at $q_f \in F$ such that the concatenation of the symbols on the path matches the input string. 

### Examples
Let $L_2 = \{w \in {0,1}^*\ |\ w\ has\ even\ numbers\ of\ 0s\ and\ 1s\}$. Construct DFA $M$ such that $L(M)=L_2$. 
