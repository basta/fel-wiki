# Vlastní hodnota (Eigenvalue)

## Summary
An eigenvalue $\lambda$ is a scalar such that for a given linear transformation or matrix $A$, there exists a non-zero vector $v$ (called an eigenvector) satisfying the equation $Av = \lambda v$.

## Detailed Explanation
In linear algebra, an **eigenvalue** (from German "eigen," meaning "own" or "characteristic") is a special scalar associated with a linear transformation or, more commonly, a square matrix. When a linear transformation acts on a non-zero vector, if the vector changes only by a scalar factor, then that scalar factor is the eigenvalue.

Specifically, for a square matrix $A$ and a non-zero vector $v$, if
$$
Av = \lambda v
$$
where $\lambda$ is a scalar, then $\lambda$ is an eigenvalue of $A$. The vector $v$ is called the **eigenvector** corresponding to the eigenvalue $\lambda$.

Eigenvalues are found by solving the characteristic equation:
$$
\text{det}(A - \lambda I) = 0
$$
where $I$ is the identity matrix of the same dimension as $A$, and $\text{det}$ denotes the determinant. The roots of this polynomial equation are the eigenvalues of the matrix $A$. Eigenvalues can be real or complex numbers.

## Importance/Relevance
With an overall importance score of 0.8, eigenvalues are a fundamental concept in linear algebra, crucial for understanding the behavior of linear transformations, analyzing dynamic systems, and in fields like quantum mechanics, engineering, and data analysis.

## Connections
This concept appears in the lecture:
*   "Diagonalisace matic" (Lecture ID: `lec_3d82103c-54e3-4c0d-b1be-9e514c5de516`)

## Category
Fundamental Concept