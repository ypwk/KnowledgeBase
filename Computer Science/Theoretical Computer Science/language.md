---
aliases: ["LANGUAGE","language","Language","Languages","languages"] 
---
Topics: #computerscience #automatatheory #finiteautomata

## Language
A languages is a set of [[word|words]]/strings. 

### Operators
Let $A$ and $B$ be two languages. 
- Union: 
	- $A\cup B=\{x\ |\ x\in A\ or\ x\in B\}$
- Concatenation: 
	- $A\cdot B=AB=\{xy\ |\ x\in A\ and\ y\in B\}$.
- Kleene Star:
	- $A^{*}=\{x_1x_2 \dots x_k\ |\ all\ k \geq 0\ and\ each\ x_i \in A\ for\ i = 1,2, \dots,k\}$.
	- Note that $\epsilon \in A^{*}$
- Intersection
	- $A\cap B=\{x|x\in A\ and\ x\in B\}$
- Complement
	- $\bar{A}$ is the set of all elements under consideration that are not in $A$. Usually, $\bar{A}=\Sigma^{*}-A$.
- Difference
	- $A-B=A\cap\bar{B}$.
- Power
	- $A^k=\{x_1x_2 \dots x_k\ |\ x_i \in A\ for\ i = 1,2, \dots,k\}=AA^{k-1}$
	- Observation:
		- $A^0=\{\epsilon\}$
		- $A^*=\{A^0 \cup A^1 \cup A^2 \cup \dots \}$ (zero or more)
		- $A^+=\{A^1 \cup A^2 \cup \dots \}$ (one or more)
		- $A^*=A^+ \cup \{\epsilon\}$

### Examples
$$
\begin{aligned}
A&=\{w|w\ has\ an\ equal\ number\ of\ 0s\ and\ 1s\}=\{\varepsilon,01,10,0011,0110,1010,\dots\}\\
B&=\{0^n1^n|n\leq1\}=\{01,0011,000111,\dots\}\\
\end{aligned}
$$
Note that $B\subset A$.