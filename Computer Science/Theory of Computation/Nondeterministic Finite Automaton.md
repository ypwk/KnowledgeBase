---
aliases: ["NONDETERMINISTIC FINITE AUTOMATON","nondeterministic finite automaton","Nondeterministic Finite Automaton","Nondeterministic Finite Automata","nondeterministic finite automata","NFA","NFAs"] 
---
Topics: #computerscience #automatatheory #finiteautomata

## Nondeterministic Finite Automaton (NFA)

### Definition
NFA $N=(Q,\Sigma,\delta,q_0,F)$, where 
- $Q$ is a finite set of states
- $\Sigma$ is an [[alphabet]]
- $q_0\in Q$ is a start state
- $F\subseteq Q$ is a set of accept/final states
- $\delta : Q \times (\Sigma \cup {\varepsilon}) \rightarrow 2^Q$ is a [[transition function]], where $\delta(q,a) = P$ is the set of states that $N$ may enter if the current state is $q$ and the current symbol is $a$.
	- If $\delta(q,\varepsilon) = P$, $N$ ignores the current symbol and goes from $q$ to any state in $P$ without reading any symbol.
	- For any $P \subseteq Q$, the $\varepsilon$-closure $E(P)$ is the set of all states reachable from any state in $P$ via 0 more more $\varepsilon$-transitions. 

Thus, this is the language recognized by a NFA $N: L(N) = \{w\ |\ \hat{\delta}(q_0,w) \cap F \neq \emptyset\}$, where $\hat{\delta}$ is an extended [[transition function]]. $L(M)$ is a [[regular language]].

### Operation
A NFA **accepts** a string if along all paths starting at $q_0$ and ending at $q_f \in F$, there is some path such that the concatenation of the symbols on the path matches the input string. 

### Graph Form
NFAs do not have the same constraints as [[Deterministic Finite Automaton|DFAs]].

### Construction from [[regular expression|regular expression]]
Since regular expressions are defined recursively, it is suitable to construct an equivalent NFA recursively, or inductively.
- Basis: Define NFAs to accept the simple regular expressions: $\varepsilon$, $\emptyset$, and $a$ for $a \in \Sigma$.
	- The NFA to decide $\varepsilon$: ![[NFA_1.jpg]] 
	- The NFA to decide $a$:
		![[NFA_2.jpg]] 
- Induction: Given the NFAs for regular expressions $a$ and $b$, define NFAs for $a \cup b$, $ab$, and $a ^{*}$. 
	- The NFA to decide $a \cup b$: ![[NFA_3.jpg]]
	- The NFA to decide $ab$: ![[NFA_4.jpg]]
	- The NFA to decide $a^{*}$: ![[NFA_5.jpg]]

