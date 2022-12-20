---
aliases: ["REDUCIBILITY","reducibility","Reducibility","reduction","reducible"] 
---
Topics: #computerscience #automatatheory #finiteautomata

## Reducibility
We say that problem $A$ reduces (or is reducible) to problem $B$, written as $A \leq B$, if we can use a solution ([[Turing Machine|TM]]) to B to solve $A$, and the conversion is done in polynomial time (i.e., if $B$ is decidable/solvable, so is $A$.). 

We may use reducibility to prove undecidability as follows: 
1. Let $A$ be [[Turing Decidable Language|non-TD]], such as $A_D$ or $A_{TM}$ . We want to prove that $B$ is non-TD. 
2. Assume $B$ is [[Turing Decidable Language|TD]]. Then there exists a TM $M_B$ to decide $B$. 
3. If we can use $M_B$ as a sub-routine to construct a TM $M_A$ that decides $A$, then $A$ is TD. We have a contradiction. 
4. The construction of TM $M_A$ using TM $M_B$ establishes that A reduces to B, i.e., $A \leq B$. (A is no harder than B) 
5. Corollary 5.23 (Sipser p. 236): If $A \leq B$ and $A$ is non-TD, then $B$ is non-TD.

### Example Proofs
The following are some proofs for non-TD by reduction. 

##### Prove that $A_{TM}$ is non-TD by reduction
1. Assume $A_{TM}$ is TD, by contradiction.
2. Let TM $S$ decide $A_{TM}$.
$$S(\langle M, w \rangle) = \begin{cases}
        accept\ w \in L(M) \\
        reject\ w \notin L(M)
    \end{cases}$$
3. Construct a TM $D$ that decides $A_D$, a [[Turing Recognizable Language|non-TR]] Language. 
<div></div>

TM $D$ = "On input $w_i$,
	Run $S$ on $\langle M_i, w_i \rangle$
	If $S$ accepts, **reject** else **accept**"

4. $S$ accepts $\langle M_i, w_i \rangle$ iff $w_i \in L(M_i)$ iff $w_i \notin A_D$ iff $D$ rejects $w_i$. So $S$ accepts iff $D$ rejects.
5. Then, $A_D$ is TD. This is a contradiction. 

##### Prove that $EQ_{TM} = \{\langle M_1, M_2 \rangle | L(M_1)=L(M_2)\}$ is non-TD by reduction
We will reduce from $E_{TM}=\{\langle M \rangle | L(M)=\emptyset\}$.
1. Assume that $EQ_{TM}$ is decided by TM $R$.
2. Construct TM $S$ that decides the undecidable $E_{TM}$. 

TM $S$ = "On input $\langle M\rangle$
	Construct TM $M_1$ = "On input $x$, immediately reject"
	Run $R$ on $\langle M_1, M\rangle$
	If $R$ accepts, **accept**; else **reject**"

3. Why does $S$ decide $E_{TM}$? $R$ accepts $\langle M_1, M\rangle$ iff $L(M_1)=L(M)$ iff $L(M)=\emptyset$ iff $S$ accepts $\langle M\rangle$.
4. S decides $E_{TM}$. So $E_{TM}$ is TD. this is a contradiction. 