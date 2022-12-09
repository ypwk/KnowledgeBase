---
aliases: ["REGULAR EXPRESSION","regular expression","Regular expression","Regular expressions","regular expressions", "REs", "RE"] 
---
Topics: #computerscience #finiteautomata #automatatheory 

## Regular Expression (RE)
Regular expressions are patterns that represent the structure of all strings in a [[regular language]]. The goal when writing a regular expression is to make it as simple and readable as possible. 

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

### Practice
The following are some practice problems related to regular expressions.

#### Design a regular expression for the following [[language]]: $\{w has no substring $10\}$
- $0^*1^*$

#### Design a regular expression for the following language: $\{w$ has an even number of 1's$\}$
- $(0^*10^*10^*)^* \cup 0^*$

#### Design a regular expression for the following language: $\{w$ has odd length$\}$
- $((0 \cup 1)(0 \cup 1))^*(0 \cup 1)$

#### Design a regular expression for the following language: $\{w$ has a 1 in the 3rd or 2nd position from the right end$\}$
	- $(0 \cup 1)^*1(0 \cup 1)(0 \cup 1)\cup(0 \cup 1)^* 1(0 \cup 1) \rightarrow$
	- $(0∪1)^*1(0∪1)((0∪1)∪ε) ⇒$
	- $(0∪1)^*1(0∪1)(0∪1∪ε)$

#### Design a regular expression for a language of strings that consist of alternating 0s and 1s:
- $(01)^* \cup (10)^* \cup 0(10)^* \cup 1(01) ^*$.

#### Design a regular expression for the following language: $D = \{ w$ has an odd number of alternating blocks of 0's and 1's$\}$.
- What are some example strings that exist and don't exist in $D$? 
	- $0|1|0 \in D, 0|1|0|1 \in D, 11|00|111 \in D, 0|11|000|11|0|1 \notin D$
- An odd number of blocks implies that [[word|strings]] in $D$ must start and end with the same symbol. 
	- From this, we can write the following regular expression: $0( \cup 1) ^{*} \cup 1 ( 0 \cup 1) ^{*}1 \cup 0 \cup 1$.
- If we draw boundaries between blocks, there is a substring $01$ or $10$ at each boundary. A string in $D$ must have the same number of $01$ and $10$. 
	- From this, we can write the following regular expression: $0^+ (1^+0^+)^* \cup 1^+(0^+1^+)^*$

#### Design a regular expression for the following language: $E=\{w|$ In $ w,$ each 1 is immediately preceeded by a 0 and followed by a 0\}$
- What are some example strings that exist in $E$? 
	- We want a substring $010$. $0010001000010010∈E$. We can rewrite this as $(001)(0001)(00001)(001)(0) ⇒ (0^+1)(0^+1)(0^+1)(0^+1)(0^+)$
- Thus, two possible regular expressions for this language could be $(0+1)^*0^+∪ε$ and $0^+(10^+)^*∪ε$.
	