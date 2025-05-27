# Gauss-Jordan Elimination

## Summary
An extension of Gaussian elimination where row operations continue until a reduced row echelon form (identity matrix) is achieved, allowing for the direct determination of a unique solution or the inverse of a matrix.

## Detailed Explanation
Gauss-Jordan elimination is an algorithmic process used to solve systems of linear equations, find the inverse of a matrix, or determine the rank of a matrix. It builds upon Gaussian elimination by further reducing the matrix.

**Definition:**
An extension of Gaussian elimination where row operations continue until a reduced row echelon form (identity matrix) is achieved, allowing for the direct determination of a unique solution or the inverse of a matrix. (Source: 06B-2024-GEM-souostavy-cast2)

Unlike Gaussian elimination, which stops at row echelon form, Gauss-Jordan elimination continues the row operations until the matrix is in *reduced* row echelon form. This means that:
*   The leading entry (pivot) in each non-zero row is 1.
*   Each pivot is the only non-zero entry in its column.
*   All zero rows are at the bottom.

When applied to an augmented matrix $[A | b]$ for solving $A * x = b$, this process directly yields the solution vector $x$ on the right side if a unique solution exists. When applied to $[A | I]$ (where $I$ is the identity matrix) for finding the inverse of $A$, it transforms into $[I | A^{-1}]$.

## Importance/Relevance
This algorithm is of high importance in linear algebra due to its systematic approach to solving linear systems and its direct utility in computing matrix inverses. It's a foundational method for many computational problems.

## Connections
This concept appears in the following lecture:
*   "GEM a soustavy lineárních rovnic, část 2" (ID: 06B-2024-GEM-souostavy-cast2)

## Category
Algorithm