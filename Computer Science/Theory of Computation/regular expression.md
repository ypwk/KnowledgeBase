---
aliases: ["REGULAR EXPRESSION","regular expression","Regular expression","Regular expressions","regular expressions", "REs", "RE"] 
---
Topics: #computerscience #finiteautomata #automatatheory 

## Regular Expression (RE)
Regular expressions are strings that represent the structure of [[regular language|regular languages]]. 

### Definition
Let $L(R)$ be the language that regular expression $R$ represents. An inductive definition is as follows:
- Basis: $\varepsilon$ and $\emptyset$ are regular expressions, and $L(\varepsilon) = \{\varepsilon\}$ and $L(\emptyset) = \emptyset$. For any $a \in \Sigma$, $a$ is a regular expression and $L(a) = \{a \}$.
- Induction: if $R_1$ and $R_2$ are regular expressions, then:
	- $R_1 \cup R_2$ is a regular expressio, with $L(R_1 \cup R_2) = L(R_1) \cup L(R_2)$.
	- $R_1R_2$ is a regular expression, with $L(R_1R_2) = L(R_1)L(R_2)$.
	- $R^{*}_1$ is a regular expression, with $L(R^{*}_1) = (L(R_1))^{*}$.
	- $(R_1)$ is  regular expression, with $L((R_1)) = L(R_1)$. 

The above four bullet points and $R^{+}$ and $R^{k}$ form the set of all operators for regular expressions. 

### Operator Precedence
The operator precedence order for regular expression operators are as follows: 
1. Parenthesis (could override the order, but not in every case)
2. Star
3. Concatenation
4. Union

### Algebraic Laws
The following are some algebraic laws for regular expressions:
- $R1\cup R2 =R2\cup R1$
- $(R1∪R2)∪R3 =R1∪(R2∪R3)$
- $(R1R2)R3 =R1(R2R3)$
- $\emptyset \cup R=R \cup \emptyset=R$
- $\varepsilon R=R \varepsilon=R$.
- $\emptyset R=R \emptyset= \emptyset$
- $R \cup R=R$
- $R1(R2 \cup R3)=R1R2 \cup R1R3$
- $(R1 \cup R2)R3 =R1R3 \cup R2R3$
- $(R^{*})^{*} =R^{*}$
- $\emptyset^{*} = \emptyset$
- $R^{+} =RR^{*} =R^{*}R$
- $R^{*}=R^{+} \cup \varepsilon$

