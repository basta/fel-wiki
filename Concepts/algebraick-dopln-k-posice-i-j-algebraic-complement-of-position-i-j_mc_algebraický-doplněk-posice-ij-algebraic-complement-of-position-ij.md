# Algebraický doplněk posice (i,j) (Algebraic complement of position (i,j))

## Summary
The algebraic complement for position $(i,j)$, denoted as $A_{ij}$, can be defined as $\text{det}(a_1, \dots, a_{j-1}, e_i, a_{j+1}, \dots, a_n)$. More practically, it is calculated as $A_{ij} = (-1)^{i+j} \cdot \text{det}(M_{ij})$, where $M_{ij}$ is the minor matrix formed by removing the $i$-th row and $j$-th column from the original matrix.

## Detailed Explanation
The algebraic complement, also known as a cofactor, is a fundamental concept in linear algebra that plays a vital role in calculating determinants via cofactor expansion and in constructing the adjoint matrix for finding the inverse of a matrix.

For an element $a_{ij}$ in a matrix $A$ (located at row $i$ and column $j$), its algebraic complement $A_{ij}$ is defined in two equivalent ways:

1.  **Using column replacement:** $A_{ij} = \text{det}(a_1, \dots, a_{j-1}, e_i, a_{j+1}, \dots, a_n)$, where $a_k$ represents the $k$-th column of matrix $A$, and $e_i$ is the $i$-th standard basis vector (a column vector with 1 in the $i$-th position and 0 elsewhere). This definition highlights the linearity property of the determinant concerning its columns.
2.  **Using minors:** Practically, the algebraic complement is calculated as $A_{ij} = (-1)^{i+j} \cdot \text{det}(M_{ij})$, where $M_{ij}$ (also known as the minor of $a_{ij}$) is the submatrix obtained by deleting the $i$-th row and $j$-th column of the original matrix $A$. The term $(-1)^{i+j}$ is a sign factor that alternates between positive and negative in a chessboard pattern across the matrix positions.

## Key Aspects/Components
*   **Minor Matrix ($M_{ij}$):** The submatrix obtained by removing the $i$-th row and $j$-th column of the original matrix.
*   **Sign Factor ($(-1)^{i+j}$):** This factor determines the sign of the cofactor based on the position $(i,j)$, ensuring the correct contribution to the determinant calculation.

## Importance/Relevance
This concept is important (overall importance score 0.8) because it is a prerequisite for understanding and applying the cofactor expansion method for determinants and for deriving the formula for the inverse of a matrix using the adjoint matrix.

## Connections
This concept appears in:
*   Lecture: "Determinant, část 2" (`07B-2024-L2`)

## Category
Definition