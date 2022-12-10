---
aliases: ["TURING MACHINE","turing machine","Turing Machine","Turing Machines","turing machines", "TM", "tm", "TMs", 'tms'] 
---
Topics: #computerscience #automatatheory #finiteautomata

## Turing Machine (TM)

### Definition
A Turing machine includes a control unit, a read-write head, and a one-way infinite tape. The read-write head can move in either direction on the tape and make changes to the tape.  

TM $M=(Q, \Sigma, \Gamma, \delta, q_0. q_{\text{accept}}, q_{\text{reject}})$.
- $Q$: The finite set of states for the control unit.
- $\Sigma$: An [[alphabet]] of input symbols, not containing the "blank symbol" $B$. 
- $\Gamma$: The complete set of tape symbols. $\Sigma \cup \{B\} \subset \Gamma$.
- $\delta$: The transition function from $Q \times \Gamma$ to $Q \times \Gamma \times D$, where $D=\{L,R\}$.
- $q_0$: The start state.
- $q_{\text{accept}}$: The accept state.
- $q_{\text{reject}}$: The reject state. 

### Configuration
We could use a string to describe the state of a Turing machine at a certain time, instead of drawing a picture of the machine. 

For example, the string $X_1 \dots X_{i-1}qX_i \dots X_n$ gives a snapshot of the Turing machine at some given time, when the current state is $q$, the tape content is $X_1 \dots X_n$, and the head is pointing to $X_i$. 

We call this string a **configuration** of the Turing machine. This is similar to how [[pushdown automata]] track their state. 

If we have a transition $\delta(q, X_i) = (p, Y, L)$, then 
- $X_1 \dots X_{i-1} q X_i \dots X_n \vdash X_1 \dots X_{i-2} p X_{i-1} Y X_{i+1} \dots X_n$. 

### Practice
1. Prove that for any Turing machine $M$ whether the language of $M$, $L(M)$, is finite.
Assume that the problem $FINITE$ is [[Turing Decidable Language|Turing decidable]], and Turing machine $R$ decides $FINITE$. $$
R(\langle M \rangle) =
	\begin{cases} 
      accept\ if\ L(M)\ is\ finite \\
      reject\ if\ L(M)\ is\ not\ finite
   \end{cases} $$
We try to use $R$ to construct a new Turing machine $S$ that decides $A_{TM}$. 

Turing machine $S=$ "On input $\langle M, w \rangle$, 
- define a Turing machine $M' =$ "On input $x$, erase $x$, then run $M$ on $w$."
- Run $R$ on $M'$. 
- If $R$ accepts, $S$ **rejects** else **accept**."

We can see that $L(M') = \Phi$ if $w \notin L(M)$, and $L(M') = \Sigma^{*}$ if $w \in L(M)$. Thus, $R$ accepts $\langle M' \rangle$ iff $L(M')$ is finite, iff $w \notin L(M)$, iff $R$ rejects. 