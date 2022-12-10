design a simple dfa to accept a simple language (p 27 class notes, p31, ex 5)
closure properties for regular languages
review regular expressions and understand their meaning
use closure properties to prove that a language is nonregular
context free grammar design (simple)
the basics of pushdown automata (limited in scope) 3 point bonus small question
closure properties for context free languages (p 96 - 98)
prove language non context free (p99, 100)

no pumping lemma proofs, for both regular languages and context free languages

problems, languages, solvable (TD) vs unsolvable (non-TD)
Turing machines, how it works, its language, its encoding, Church-Turing thesis
Turing Recognizable (input given is in languages, just need a Turing Machine to verify)
Turing Decidable (input given can be any string. Need a stronger Turing Machine to check if it is in the language (accept) or not in the language (reject))
The meaning of reduction A <=p B means that A is no harder than B or B is at least as hard as A
- comparing degree of difficulty in the two problems
Proofs: a language is TR, TD, or non-TD
A language and its complement (p 122) (True or false, what class is the language in?) 
- If a language is TDL, then its complement must become TDL. 

(never ask to design a Turing Machine from delta function)


100 points, 6 bonus points
- Short questions about automata theory (25 points)
- T or F (Turing machines, turing recognizability, turing decidability, special languages ($A_{TM}$, $HALT_{TM}$)) (24 points)
- Proof of undecidability and some short questions about some languages and their complement (17 points)
- Short questions about P and NP (24 points)
- proof of a decision problem to be in NP ( 4 points)
	- One sentence proof that needs to include four keywords
- two bonus questions about CFG and PDA (6 bonus points)

Baeldung P, NP diagram :) with the increasing difficulty

## Sample Problems 
1. The universal language $A_{TM}$ is a subset of the language $HALT_{TM}$. 
	- True — $HALT_{TM}$ concerns whether a language accepts, while $A_{TM}$ concerns whether a language decides.  
2. Let $L$ be [[Turing Recognizable Language|Turing recognizable]] but not [[Turing Decidable Language|Turing decidable]], then $\bar{L}$ is [[Turing Recognizable Language|non-TR]]. 
	- True — trivial, from the language and complement relationship. 
3. If $A$ is non-TD and $A \leq C$ and $D \leq C$, then $D$ is non-TR.
	- False — C is more difficult than A, 
4. A problem that can be solved by a [[Deterministic Turing Machine]] in $2^n$ steps must be intractable (run in exponential time) 
	- False? She said it was unclear?? This is so vague and shitty. Depends on the size of $n$ —  at small $n$, it isn't that bad
		- We could write a shitty DTM that solves an easy problem in $2^n$ steps. 
1. If $\Pi_1 \notin NP$, then $\Pi_1$ may still be in $P$. 
	- False —  any problem $\Pi$ that is in $P$ must also be in $NP$. 
2. If $A \leq_{P} B$, then it is possible that $A \in P$ but $B \notin NP$. 
	- True — 
3. If $\Pi_{1} \leq_{P} \Pi_{2}$ and $\Pi_1 \in NP$, is  $\Pi_2 \in NP$?
	- False — $\Pi_2$ is as least as hard as $\Pi_1$.
4. If $\Pi_{1} \leq_{P} \Pi_{2}$ and $\Pi_1, \Pi_2 \in NPC$, is $\Pi_{2} \leq_{P} \Pi_{1}$ ?
	- True — 
9.  If $\Pi_{1} \leq_{P} \Pi_{2}$ and $\Pi_1 \notin NP$, is $\Pi_{1} \in P$ ?
	-  False 