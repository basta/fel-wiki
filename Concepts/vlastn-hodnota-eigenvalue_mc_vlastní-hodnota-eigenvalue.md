# Vlastní hodnota (Eigenvalue)

## Summary
For a linear transformation $f : L \rightarrow L$, $\lambda$ in $F$ is an eigenvalue (also: characteristic value) if there exists a non-zero vector $x$ satisfying the equality $f(x) = \lambda \cdot x$.

## Detailed Explanation
An **eigenvalue** (also known as a **characteristic value**) is a special scalar associated with a linear transformation (or a square matrix). For a given linear transformation $f$ from a vector space $L$ to itself, a scalar $\lambda$ (from the field $F$, typically real or complex numbers) is an eigenvalue if there exists a non-zero vector $x$ in $L$ such that when $f$ acts on $x$, the result is simply a scalar multiple of $x$. This relationship is expressed by the equation:
$$f(x) = \lambda \cdot x$$
In matrix form, if $A$ is the matrix representation of $f$, this equation becomes $Ax = \lambda x$, or equivalently $(A - \lambda I)x = 0$, where $I$ is the identity matrix. The existence of a non-zero vector $x$ for this equation implies that the matrix $(A - \lambda I)$ must be singular, meaning its determinant is zero: $\det(A - \lambda I) = 0$. This equation is known as the characteristic equation, and its roots are the eigenvalues.

## Importance/Relevance
With an overall importance score of 1.0, the concept of eigenvalues is fundamental and critical in linear algebra. Eigenvalues provide crucial information about the behavior of linear transformations, revealing directions along which the transformation acts merely as a scaling operation. They are extensively used in various fields including physics (quantum mechanics, stability analysis), engineering (vibrational analysis, signal processing), computer graphics, and statistics (principal component analysis).

## Connections
This concept appears in the following lectures:
*   "Vlastní hodnoty a vlastní vektory" (lecture-eigenvalues-eigenvectors-08a-2024)

There are no known aliases for this term.

## Category
Fundamental Concept