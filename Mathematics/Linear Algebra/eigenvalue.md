---
aliases: ["EIGENVALUE","eigenvalue","Eigenvalue","Eigenvalues","eigenvalues"] 
---
Topics: #mathematics #linearalgebra

## Eigenvalue
Given a square matrix $A \in M_n$, an eigenvalue of $A$, $\lambda \in \mathbb{R}$, satisfies the eigenvalue-eigenvector equation: $Ax = \lambda x$, where $\lambda$ is the eigenvalue and $x \neq 0$ is the [[eigenvector]]. 

### Calculating Eigenvalues 
Let  $A = \begin{bmatrix} 5 & -1 \\ 2 & 2 \end{bmatrix}$. Note that the row sums of $A$ are all 4. We can infer the following: $$
\begin{bmatrix} 5 & -1 \\ 2 & 2 \end{bmatrix} \begin{bmatrix}
1 \\ 1
\end{bmatrix} = \begin{bmatrix}
 4\\ 4
\end{bmatrix} = 4\begin{bmatrix}
1 \\ 1
\end{bmatrix}
$$Thus, 4 is an eigenvalue for $A$, and $\begin{bmatrix} 1 \\ 1\end{bmatrix}$ is an [[eigenvector]] for $A$ associated with the eigenvalue 4. Using the [[trace]] (7) and [[determinant]] (12), the other eigenvalue must be 3. Since the eigenvector of a matrix remains an eigenvector of that matrix after scalar multiplication, we can set the first entry of the eigenvector associated with 3 to 1:  $$
\begin{bmatrix} 5 & -1 \\ 2 & 2 \end{bmatrix} \begin{bmatrix}
1 \\ x
\end{bmatrix}
$$After calculation, $x$ in this case must be 2. Thus, the eigenvector associated with 3 must be $\begin{bmatrix} 1 \\ 2\end{bmatrix}$.
