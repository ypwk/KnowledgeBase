---
aliases: ["MATRIX POLYNOMIAL","matrix polynomial","Matrix polynomial"] 
---
Topics: #mathematics #linearalgebra 

## Matrix polynomial
Let $p(t)$ be a polynomial of degree $k$. Then $p(t)$ is of the following form: $$p(t) = a_n t^n + a_{n-1} t^ {n-1} + \dots + a_1 t + a_0$$ Then $p(A) = a_nA^n + a_{n-1} A^ {n-1} + \dots + a_1 A + a_0$.

If $\lambda$ and $x$ are an [[eigenvalue]] and [[eigenvector]] of the [[matrix]] $A \in \mathbb{M}_n$, then $p(\lambda)$ and $x$ are an eigenvalue and eigenvector of $p(A)$.

In other words, if you substitute a matrix into a polynomial, the resulting matrix polynomial will have eigenvalues equal to the eigenvalues of the matrix evaluated at the polynomial, and will have eigenvectors equal to the eigenvectors of the original matrix. 

The eigenvectors of the matrix polynomial will appear with the same multiplicity as the eigenvalues of the original matrix. 