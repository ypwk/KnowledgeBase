---
aliases: ["TURING RECOGNIZABLE LANGUAGE","turing recognizable language","Turing Recognizable Language","Turing Recognizable Languages","turing recognizable languages", "TRL", "TRLs", "TR", "non-TR", "Turing recognizable"] 
---
Topics: #computerscience #automatatheory #finiteautomata

## Turing Recognizable Language (TRL)
A [[language]] $A$ is Turing-recognizable if there is a [[Turing Machine|TM]] $M$ such that $A=L(M)$. 

In other words, $∀w ∈A$, $M$ accepts $w$ by entering $q_{\text{accept}}$. $∀w \notin A$, $M$ does not accept (i.e., it may reject or loop).
