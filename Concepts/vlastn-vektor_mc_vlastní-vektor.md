# Vlastní vektor (Eigenvector)

## Summary
An eigenvector $v$ is a non-zero vector that, when a linear transformation or matrix $A$ is applied to it, results in a vector that is a scalar multiple of $v$ itself. The scalar factor is known as the eigenvalue.

## Detailed Explanation
An **eigenvector** is a special non-zero vector that, when a linear transformation or a matrix $A$ operates on it, simply gets scaled by a scalar factor, without changing its direction (or only reversing it). This relationship is expressed by the fundamental equation:
$$
Av = \lambda v
$$
Here:
*   $A$ is a square matrix or a linear transformation.
*   $v$ is the non-zero eigenvector.
*   $\lambda$ is the corresponding **eigenvalue** (the scalar factor).

The "eigen" prefix is from German, meaning "own" or "characteristic," highlighting that these vectors are inherent to the matrix/transformation. Eigenvectors reveal the directions along which the linear transformation acts simply by stretching or compressing.

For a given eigenvalue $\lambda$, the set of all eigenvectors corresponding to $\lambda$, along with the zero vector, forms a subspace called the **eigenspace** of $\lambda$. This eigenspace consists of all vectors $v$ that satisfy $(A - \lambda I)v = 0$, where $I$ is the identity matrix.

## Importance/Relevance
With an overall importance score of 0.8, eigenvectors are fundamental concepts in linear algebra, providing critical insights into the dynamics and structure of linear transformations, used extensively in fields like physics, engineering, computer graphics, and machine learning.

## Connections
This concept appears in the lecture:
*   "Diagonalisace matic" (Lecture ID: `lec_3d82103c-54e3-4c0d-b1be-9e514c5de516`)

## Category
Fundamental Concept