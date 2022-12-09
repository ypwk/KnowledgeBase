---
aliases: ["POLYNOMIAL REDUCTION","polynomial reduction","Polynomial reduction"] 
---
Topics: #computerscience #finiteautomata #computabilitytheory 

## Polynomial Reduction ($\leq_{p}$)

Let $\Pi_1$ and $\Pi_2$ be two decision problems, and $\{l_1\}$ and $\{l_2\}$ be sets of instances for $\Pi_1$ and $\Pi_2$, respectively. We say that there is a **polynomial reduction** from  $\Pi_1$ to $\Pi_2$, or  $\Pi_1 \leq_p \Pi_2$, if there is a function $f : \{l_1\} \rightarrow \{l_2\}$ such that $f$ can be computed in polynomial time and $l_1$ has a "yes" solution if and only if $f(l_1)$ has a "yes" solution. 

$\leq_p$ can be thought of as "no harder than". 

### Theorems
- If $\Pi_1 \leq_p \Pi_2$, then $\Pi_2 \in$ [[class of P|P]] implies that $\Pi_1 \in P$. 
- If $\Pi_1 \leq_p \Pi_2$ and $\Pi_2 \leq_p \Pi_3$, then $\Pi_1 \leq_p \Pi_3$. 
