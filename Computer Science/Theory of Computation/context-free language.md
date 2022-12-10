---
aliases: ["CONTEXT-FREE LANGUAGE","context-free language","Context-free language","Context-free languages","context-free languages","CFL","CFLs"] 
---
Topics: #computerscience #finiteautomata #automatatheory #principlesprogramminglanguages

## Context-free Language (CFL)
The language of a [[context-free grammar]] $G$ is $L(G)=\{w \in \Sigma^*\ |\ S \xRightarrow{*} w\}$. $L(G)$ is said to be a context-free language. 

### Closure Properties
- Union
	- If $A$ and $B$ are both context-free, so is $A \cup B$.
	- Proof:
		- Given context-free grammars $G_A$ with $S_A \rightarrow \dots$ and $G_B$ with $S_b \rightarrow \dots$, we can define a context-free gammar that generates $A \cup B$ as $S \rightarrow S_A | S_B$ plus the grammars $G_A$ and $G_B$. 
- Concatenation
	- If $A$ and $B$ are both context-free, so is $AB$. 
	- Proof:
		- Given context-free grammars $G_A$ with $S_A \rightarrow \dots$ and $G_B$ with $S_b \rightarrow \dots$, we can define a context-free grammar that generates $AB$ as $S \rightarrow S_AS_B$ plus the gammars $G_A$ and $G_B$. 
- Star
	- If $A$ is context-free, so is $A^*$.
	- Proof:
		- Given a context-free grammar $G$ with $S_1 \rightarrow \dots$, we can define a context-free grammar that generates $A^*$ as $S \rightarrow SS_1 | \varepsilon$ plus the grammar $G$. 
- Reverse
	- If $A$ is context-free, so is $A^R$. 
- Intersection with a [[regular language]]
	- If $A$ is context-free and $B$ is regular, then $A \cap B$ is context-free. 
- Difference from a [[regular language]]
	- If $A$ is context-free and $B$ is regular, then $A-B$ is context-free.