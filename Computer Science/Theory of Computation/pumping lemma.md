---
aliases: ["PUMPING LEMMA","pumping lemma","Pumping lemma","PL"] 
---
Topics: #computerscience #automatatheory #finiteautomata 

## Pumping Lemma

The pumping lemma is a condition that can be applied to regular languages and context-free languages to prove that they are nonregular or not context-free. 

### [[Regular Language]]
For any regular language $A$, there exists a constant $p$ (whose value depends on $A$) such that $\forall s \in A$ with $|s| \geq p$, $s$ can be partitioned into three substrings $s=xyz$ such that $|y| > 0|$, $|xy| \leq p$, and the string $xy^iz \in A : \forall i \geq 0$, where $y^i$ is the $i$th power of $y$.

#### Boilerplate Proof
1. Assume that $A$ is regular by contradiction. 
2. Thus, the pumping lemma applies to $A$.
3. Let $p$ be the constant in the pumping lemma. 
4. Select $s \in A$ with $|s|=f(p) \geq p$.
5. By the pumping lemma, $\exists x,y,z$ such that $s=xyz$ with $|y| > 0$,  $|xy| \leq p$, and $xy^iz \in A:\forall i \geq 0$.
6. For any $x, y, z$ such that $s = xyz$, $|y| > 0$ and $|xy| \leq p$, find $i \geq 0$ such that $xy^iz \notin A$.
7. This is a contradiction, so $A$ must be nonregular.

###  [[Context-Free Language]]
For any context-free language A, there exists a constant $p$ such that $\forall s \in A$ with $|s| \geq p$, $s$ can be partitioned into five substrings $s=uvxyz$ such that $|vy| > 0$ with $v, y \neq \varepsilon$, $|vxy| \leq p$, and the string $uv^ixy^iz \in A:\forall i \geq 0$. 

#### Boilerplate Proof
1. Assume that $A$ is context-free by contradiction. 
2. Thus, the pumping lemma applies to $A$.
3. Let $p$ be the constant in the pumping lemma. 
4. Select $s \in A$ with $|s|=f(p) \geq p$. (This could be difficult, but start with an intuitive simple string that uses $p$ in the length)
5. By the pumping lemma, $\exists u,v,x,y,z$ such that $s=uvxyz$ with $|vy| > 0$,  $|vxy| \leq p$, and $uv^ixy^iz \in A:\forall i \geq 0$. 
6. For any $u, v, x, y, z$ such that $s = uvxyz$, $|vy| > 0$ and $|vxy| \leq p$, find $i \geq 0$ such that $uv^ixy^iz \notin A$.
7. This is a contradiction, so $A$ must be nonregular.



### Practice
The following are some practice problems using the pumping lemma. 

#### Prove that $B=\{0^{n}1^{n}|n \geq 0\}$ is not regular. 
1. Assume $B$ is a regular language. 
2. Then the pumping lemma applies to $B$. 
3. Let $p$ be the constant in the pumping lemma.
4. Select $s=0^{p}1^{p} \in B$ with $|s|=2p>p$.
5. By the pumping lemma, $s=0 \dots 0 1 \dots 1=xyz$, $|y|>0$ and $|xy| \leq p$. Since $y \neq \varepsilon$ and $|xy| \leq q$, then $y = 0^{+}$. 
6. Choose $i=0$. Then $xy^0z=xz=0^{p'}1^p$ for $p' < p$. Thus, $xy^0z \notin B$. 
7. This a contradiction to the pumping lemma, so $B$ is nonregular. 

#### Prove that $F = \{ww|w \in \{0, 1\}^{*}\}$ is not regular. 
1. Assume $F$ is a regular language.
2. Then the pumping lemma applies to $F$. 
3. Let $p$ be the constant in the pumping lemma. 
4. Select $s =0^p10^p1 \in F$ with $|s|=2p+2>p$.
5. By the pumping lemma, $s =0 \dots 0 10 \dots 0 1=xyz$, $|y|>0$, $|xy|??? p$. Since $y=??$ and $|xy|???p$, then $y =0^+$ 
6. Choose $i =2$. Then $xy^2z=xyyz=0^{p'}10^p1$ for $p'>p$. Thus, $xy^2z \notin F$. 
7. A contradiction to the pumping lemma. So $F$ is nonregular. 