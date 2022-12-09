---
aliases: ["CLASS OF NPC","class of npc","Class of NPC", "NPC"] 
---
Topics: #computerscience #finiteautomata #computabilitytheory 

## Class of NP-complete (NPC)

The class of NPC, or NP-complete, is the class of the hardest problems in [[class of NP|NP]]

There are two definitions for a problem $\Pi \in NPC$:
- $\Pi \in NPC$ if $\Pi \in NP$ and $\forall \Pi' \in NP$, $\Pi' \leq_p \Pi$. 
- $\Pi \in NPC$ if $\Pi \in NP$ and $\exists \Pi' \in NPC$, $\Pi' \leq_p \Pi$. 
Thus, to show that a problem $\Pi \in NPC$, prove that $\Pi \in$ [[class of NP|NP]] and that $\exists \Pi' \in NPC$ such that $\Pi' \leq_p \Pi$.

### Theorems
- If $\exists \Pi \in NPC$ such that $\Pi \in P$, then [[class of P|P]]=[[class of NP|NP]].
- If $\exists \Pi \in NPC$ such that $\Pi \notin P$, then $P \neq NP$.