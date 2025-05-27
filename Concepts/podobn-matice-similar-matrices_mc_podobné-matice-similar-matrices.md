# Podobné matice (Similar Matrices)

## Summary
Two square matrices A and B are similar if $B = T^{-1}AT$ for some invertible matrix T. Similar matrices represent the same linear transformation with respect to different bases.

## Detailed Explanation
Two square matrices, A and B, are considered **similar matrices** if there exists an invertible matrix T such that the relationship $B = T^{-1}AT$ holds. This definition is crucial in linear algebra because it signifies a profound connection between the matrices.

### Definitions
*   **Definition 1 (from lec-coordinate-transformation-matrices-05B-2024):** Two square matrices A and B are similar if $B = T^{-1}AT$ for some invertible matrix T. Similar matrices represent the same linear transformation with respect to different bases.

In essence, similar matrices represent the *same linear transformation*, but their entries are expressed with respect to *different bases*. The matrix T acts as a change-of-basis matrix, transforming the coordinates from one basis to another, thereby transforming the matrix representation of the linear operator.

## Importance/Relevance
This concept is of very high importance in linear algebra as it clarifies how a linear transformation can be represented by different matrices depending on the chosen basis. Understanding similar matrices is foundational for topics like diagonalization, eigenvalues, and eigenvectors, where simplifying the matrix representation of a linear transformation is key.

## Connections
### Appears in Lectures
*   [Transformace souřadnic](lec-coordinate-transformation-matrices-05B-2024)

### Category
Matrix Property