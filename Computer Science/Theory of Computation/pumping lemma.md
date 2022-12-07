---
aliases: ["PUMPING LEMMA","pumping lemma","Pumping lemma","PL"] 
---
Topics: #computerscience #automatatheory #finiteautomata 

## Pumping Lemma

### Regular Languages
The pumping lemma when applied to [[regular language|regular languages]], is used to prove that [[language]] is nonregular. 

##### Theorem
For any regular language $A$, there exists a constant $p$ (whose value depends on $A$) such that $\forall s \in A$ with $|s| \geq p$, $s$ can be partitioned into three substrings $s=xyz$ such that $|y| > 0|$, $|xy| \leq p$, and the string $xy^iz \in A : \forall i \geq 0$, where $y^i$ is the $i$th power of $y$.

##### Boilerplate Proof
1. Assume that $A$ is regular by contradiction. 
2. Thus, the pumping lemma applies to $A$.
3. Let $p$ be the constant in the pumping lemma. 
4. Select $s \in A$ with $|s|=f(p) \geq p$.
5. By the pumping lemma, $\exists x,y,z$ such taht $s=xyz$ with $|y| > 0$,  $|xy| \leq p$, and $xy^iz \in A:\forall i \geq 0$.
6. For any $x, y, z$ such that $s = xyz$, $|y| > 0$ and $|xy| \leq p$, find $i \geq 0$ such tath $xy^iz \notin A$.
7. This is a contradiction, so $A$ must be nonregular.