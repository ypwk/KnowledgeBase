---
aliases: ["PUSHDOWN AUTOMATA","pushdown automata","Pushdown automata","Pushdown automatas","pushdown automatas","PDA","PDAs"] 
---
Topics: #computerscience #finiteautomata #automatatheory 

## Pushdown Automata (PDA)

### Definition
A pushdown automata is a combined [[Nondeterministic Finite Automaton|nondeterministic finite automaton]] and a [[stack]]. 

PDA $M=(Q,\Sigma, \Gamma, \delta, q_0, F)$.
- $Q$: A finite set of states. 
- $\Sigma$: An [[alphabet]] (a finite set of symbols) for input.
- $\Gamma$: An [[alphabet]] (a finite set of symbols) for the stack.
- $\delta$: The transition function from $Q \times (\Sigma \cup {\varepsilon}) \times (\Gamma \cup {\varepsilon})$ to $2^{Q \times (\Gamma \times {\epsilon})}$.
- $q_0$: The start state.
- $F$: The set of final states.

The language of a PDA $M$ is $L(M) = \{w|(q_0, w, \varepsilon) \overset{*}{\vdash} (f, \varepsilon, \gamma) \text{ for } f \in F\}$. This is a language recognized by $M$. 

### Delta Function 
The delta function for a PDA is much more complex than the delta function for a [[Deterministic Finite Automaton|DFA]] or [[Nondeterministic Finite Automaton|NFA]]. Take, for example, the following transition: $\delta(q, a, X) = \{(p, Y)\}$. What does it mean? If the current state is $q$, the current input symbol is $a$, and the stack symbol at the top of the stack is $X$, then the automaton changes to state $p$ and the top symbol in the stack is changed from $X$ to $Y$. The following list contains some possible transitions in a delta function:
- $\delta(q, \varepsilon, X)=\{(p,Y)\}$: The cursor does not move. The top symbol in the stack is changed from $X$ to $Y$.  
-  $\delta(q, a, \varepsilon)=\{(p,Y)\}$: The cursor moves to the next symbol. $Y$ is pushed onto the stack. 
-  $\delta(q, a, X)=\{(p,\varepsilon)\}$: The cursor moves to the next symbol. $X$ is popped from the top of the stack. 
-  $\delta(q, \varepsilon, \varepsilon)=\{(p,Y)\}$: The cursor does not move. $Y$ is pushed onto the stack. 
-  $\delta(q, a, \varepsilon)=\{(p, \varepsilon)\}$: The cursor moves to the next symbol. Nothing happens to the stack. 
-  $\delta(q, \varepsilon, X)=\{(p,\varepsilon)\}$: The cursor does not move. $X$ is popped from the top of the stack. 
-  $\delta(q, \varepsilon, \varepsilon)=\{(p,\varepsilon)\}$: The only thing that changes is the state, $q$ to $p$. 

At the beginning of any computation, the PDA will push a special symbol to the initially empty stack with transition $\delta(q_0, \varepsilon, \varepsilon)=\{(q, \$)\}$ When the PDA reads a $\$$ from the stack, it knows that it is empty. 

### State Diagram
For a transition $\delta(q,a,X)=\{(p, Y)\}$, add an arc from state $q$ to state $p$ labeled with "$X \longrightarrow Y$" to the state diagram. 

### Instantaneous Description
An instantaneous description (ID) of a PDA follows the following format: $(q,w,\gamma)$. It represents the configuration of the pushdown automata. 
- $q$: Current state.
- $w$: Input left to be read as such — $w_0w_1 \dots w_i$ — where $w_0$ is the next symbol to be read. 
- $\gamma$: Content left in the stack as such — $\gamma_0\gamma_1\dots\gamma_i$ — where $\gamma_0$ is the top symbol in the stack. 

### Binary Relation ($\vdash$)
A binary relation is an operator for instantaneous descriptions. $(q, aw, X \beta) \vdash (p, w, Y \beta)$ if $\delta(q, a, X)$ contains $(p, Y)$. $\vdash$ represents one move of the PDA, and $\overset{*}{\vdash}$ represents zero or more moves of the PDA. 

### Theorems
Any PDA has an associated [[context-free grammar]] and [[context-free language]]. These three concepts are equivalent. 