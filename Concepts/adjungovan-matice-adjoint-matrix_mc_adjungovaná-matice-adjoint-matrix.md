# Adjungovaná matice (Adjoint matrix)

## Summary
For a matrix $A$, its adjoint matrix, denoted as $\text{adj}(A)$, is defined as the transpose of the matrix of its algebraic complements (cofactors).

## Detailed Explanation
The adjoint matrix, also frequently referred to as the adjugate matrix, is a specific matrix derived from another square matrix. It plays a crucial role in the analytical formula for finding the inverse of a matrix.

Given a square matrix $A = (a_{ij})$, the process of forming its adjoint matrix $\text{adj}(A)$ involves two main steps:

1.  **Forming the Cofactor Matrix:** First, construct a matrix $C = (A_{ij})$, where each element $A_{ij}$ is the algebraic complement (cofactor) of the corresponding element $a_{ij}$ from the original matrix $A$. The algebraic complement $A_{ij}$ is calculated as $A_{ij} = (-1)^{i+j} \cdot \text{det}(M_{ij})$, where $M_{ij}$ is the minor matrix obtained by removing the $i$-th row and $j$-th column of $A$.

    The matrix of cofactors is:
    $$
    C = \begin{pmatrix}
    A_{11} & A_{12} & \dots & A_{1n} \\
    A_{21} & A_{22} & \dots & A_{2n} \\
    \vdots & \vdots & \ddots & \vdots \\
    A_{n1} & A_{n2} & \dots & A_{nn}
    \end{pmatrix}
    $$

2.  **Transposing the Cofactor Matrix:** The adjoint matrix $\text{adj}(A)$ is then the transpose of this cofactor matrix $C^T$:
    $$
    \text{adj}(A) = C^T = \begin{pmatrix}
    A_{11} & A_{21} & \dots & A_{n1} \\
    A_{12} & A_{22} & \dots & A_{n2} \\
    \vdots & \vdots & \ddots & \vdots \\
    A_{1n} & A_{2n} & \dots & A_{nn}
    \end{pmatrix}
    $$

The most important property of the adjoint matrix is its relationship with the inverse of $A$: $A \cdot \text{adj}(A) = \text{adj}(A) \cdot A = \text{det}(A) \cdot I$, where $I$ is the identity matrix. This directly leads to the formula for the inverse of a matrix: $A^{-1} = \frac{1}{\text{det}(A)} \text{adj}(A)$, provided that $\text{det}(A) \neq 0$.

## Key Aspects/Components
*   **Algebraic Complements (Cofactors):** The adjoint matrix is built upon these individual cofactor values for each position in the matrix.
*   **Transpose Operation:** The final step of transposing the cofactor matrix is crucial for correctly forming the adjoint matrix.

## Importance/Relevance
The adjoint matrix is important (overall importance score 0.8) because it provides a direct, analytical method for computing the inverse of a square matrix, especially useful in theoretical contexts and for smaller matrices.

## Connections
This concept appears in:
*   Lecture: "Determinant, část 2" (`07B-2024-L2`)

## Category
Definition