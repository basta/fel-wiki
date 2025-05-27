# Determinant (det(A))

## Summary
The lecture revisits the definition of the determinant of a square matrix (using permutations) and its linearity in each column. It also highlights properties like $\text{det}(A^T) = \text{det}(A)$, $\text{det}(AB) = \text{det}(A)\text{det}(B)$, $\text{det}(A^{-1}) = (\text{det}(A))^{-1}$, and $\text{det}(aA) = a^n \text{det}(A)$.

## Detailed Explanation
The determinant of a square matrix, often denoted as $\text{det}(A)$ or $|A|$, is a scalar value that can be computed from the elements of a square matrix. It is a fundamental concept in linear algebra that encapsulates various properties of the matrix, such as its invertibility and the volume scaling factor of the linear transformation it represents.

The definition of the determinant typically involves permutations of matrix elements, and it is known for its linearity in each column (or row). The lecture specifically revisits this definition using permutations.

Key properties of the determinant highlighted include:
*   **Transpose Property:** The determinant of a matrix's transpose is equal to the determinant of the original matrix: $\text{det}(A^T) = \text{det}(A)$.
*   **Multiplicative Property:** The determinant of a product of two square matrices is the product of their determinants: $\text{det}(AB) = \text{det}(A)\text{det}(B)$.
*   **Inverse Property:** If a matrix $A$ is invertible, the determinant of its inverse is the reciprocal of its determinant: $\text{det}(A^{-1}) = (\text{det}(A))^{-1}$.
*   **Scalar Multiplication Property:** If a matrix $A$ is multiplied by a scalar $a$, the determinant of the resulting matrix is $a^n$ times the determinant of $A$, where $n$ is the dimension of the square matrix: $\text{det}(aA) = a^n \text{det}(A)$.

## Importance/Relevance
The determinant is a highly important concept in linear algebra, indicated by its overall importance score of 1.0. It is crucial for determining if a matrix is invertible, calculating inverses, understanding the geometric interpretation of linear transformations (e.g., volume scaling), and solving systems of linear equations.

## Connections
This concept appears in:
*   Lecture: "Determinant, část 2" (`07B-2024-L2`)

## Category
Fundamental Concept