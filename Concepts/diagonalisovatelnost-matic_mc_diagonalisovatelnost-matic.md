# Diagonalisovatelnost matic (Diagonalizability of Matrices)

## Summary
Diagonalizability is the property of a square matrix $A$ being similar to a diagonal matrix $D$, meaning $A = T D T^{-1}$ for some invertible matrix $T$. For matrices over the complex numbers ($\mathbb{C}$), $A$ is diagonalizable if and only if for every complex eigenvalue $\lambda$, its algebraic multiplicity (as a root of the characteristic polynomial) equals the geometric multiplicity (the dimension of its eigenspace). For matrices over real numbers ($\mathbb{R}$), this condition is more restrictive, as eigenvalues must also be real.

## Detailed Explanation
A square matrix $A$ is said to be **diagonalizable** if it is similar to a diagonal matrix $D$. This means there exists an invertible matrix $T$ such that:
$$
A = T D T^{-1}
$$
where $D$ is a diagonal matrix. The diagonal entries of $D$ are the eigenvalues of $A$, and the columns of $T$ are the corresponding linearly independent eigenvectors.

The conditions for diagonalizability depend on the field over which the matrix is defined:

*   **Over Complex Numbers ($\mathbb{C}$):** A matrix $A$ is diagonalizable over $\mathbb{C}$ if and only if for every eigenvalue $\lambda$:
    *   The **algebraic multiplicity** of $\lambda$ (its multiplicity as a root of the characteristic polynomial) is equal to its **geometric multiplicity** (the dimension of the eigenspace corresponding to $\lambda$).
    *   Equivalently, $A$ is diagonalizable if and only if there exists a basis of eigenvectors for the vector space.

*   **Over Real Numbers ($\mathbb{R}$):** For a matrix $A$ to be diagonalizable over $\mathbb{R}$, in addition to the condition above (equality of algebraic and geometric multiplicities), all eigenvalues of $A$ must be real numbers. If a real matrix has complex non-real eigenvalues, it cannot be diagonalized over $\mathbb{R}$.

Diagonalization simplifies many matrix operations, such as computing powers of a matrix ($A^k = T D^k T^{-1}$) or the matrix exponential ($e^A = T e^D T^{-1}$).

## Importance/Relevance
With an overall importance score of 0.95, Diagonalizability is a core principle in linear algebra, simplifying many computations and providing deep insights into the structure and behavior of linear transformations.

## Connections
This concept appears in the lecture:
*   "Diagonalisace matic" (Lecture ID: `lec_3d82103c-54e3-4c0d-b1be-9e514c5de516`)

## Category
Core Principle