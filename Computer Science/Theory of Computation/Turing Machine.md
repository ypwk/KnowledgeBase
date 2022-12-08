---
aliases: ["TURING MACHINE","turing machine","Turing Machine","Turing Machines","turing machines", "TM", "tm", "TMs", 'tms'] 
---
Topics: #computerscience #automatatheory #finiteautomata

## Turing Machine (TM)




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