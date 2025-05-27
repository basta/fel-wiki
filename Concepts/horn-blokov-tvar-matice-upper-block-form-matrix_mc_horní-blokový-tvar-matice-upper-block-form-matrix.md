# Horní blokový tvar matice (Upper block form matrix)

## Summary
A matrix form where every non-zero row is above any row of all zeros, and the first non-zero element ([pivot](#mc_pivot)) of each non-zero row is always to the right of the pivot of the row above it.

## Detailed Explanation
The "upper block form matrix," also known as row echelon form, is a specific type of matrix obtained through a series of [elementary row operations](#mc_řádkové-elementární-úpravy-elementary-row-operations). This form is highly desirable because it simplifies the process of solving systems of linear equations, especially when using methods like [Gaussian Elimination](#mc_gaussova-eliminační-metoda-gem).

*   **Definition:** A matrix form where every non-zero row is above any row of all zeros, and the first non-zero element (pivot) of each non-zero row is always to the right of the pivot of the row above it. (Source: 06A-2024-GEM-LinearSystems-Part1)

The key characteristics of a matrix in upper block (row echelon) form are:
1.  All non-zero rows are above any rows of all zeros.
2.  The leading entry (the first non-zero element from the left, also called the [pivot](#mc_pivot)) of each non-zero row is to the right of the leading entry of the row above it.
3.  All entries in a column below a leading entry are zeros.

Example of a matrix in upper block form:
$$
\begin{pmatrix}
1 & 2 & 3 & 4 \\
0 & 5 & 6 & 7 \\
0 & 0 & 8 & 9 \\
0 & 0 & 0 & 0
\end{pmatrix}
$$
Here, the pivots are 1, 5, and 8.

## Importance
This concept is of *high importance* (score: 0.85) as it is the target form for matrix reduction algorithms like Gaussian Elimination, enabling straightforward solution of linear systems through back-substitution and providing insights into the rank and nullity of matrices.

## Connections
This concept appears in the following lectures:
*   [GEM a soustavy lineárních rovnic, část 1](06A-2024-GEM-LinearSystems-Part1)

## Category
Mathematical Concept