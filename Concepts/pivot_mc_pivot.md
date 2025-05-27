# Pivot

## Summary
The first non-zero element from the left in a non-zero row of a matrix in upper block (row echelon) form.

## Detailed Explanation
In the context of matrix operations, particularly when transforming a matrix into its [upper block (row echelon) form](#mc_horní-blokový-tvar-matice-upper-block-form-matrix) using [Gaussian Elimination](#mc_gaussova-eliminační-metoda-gem), a *pivot* refers to a specific entry in the matrix that plays a critical role in the reduction process.

*   **Definition:** The first non-zero element from the left in a non-zero row of a matrix in upper block (row echelon) form. (Source: 06A-2024-GEM-LinearSystems-Part1)

Pivots are essential for systematically eliminating entries below them, leading to the desired triangular or echelon form. They guide the application of [elementary row operations](#mc_řádkové-elementární-úpravy-elementary-row-operations). The columns containing pivots are often referred to as pivot columns.

Example:
For a matrix in row echelon form:
$$
\begin{pmatrix}
\mathbf{1} & 2 & 3 \\
0 & \mathbf{4} & 5 \\
0 & 0 & \mathbf{6}
\end{pmatrix}
$$
The pivots are the elements 1, 4, and 6.

## Importance
This concept is of *high importance* (score: 0.7) as pivots are central to the process of Gaussian Elimination and other matrix reduction techniques. They define the structure of the row echelon form and are crucial for determining the rank of a matrix and the number of free variables in a system of linear equations.

## Connections
This concept appears in the following lectures:
*   [GEM a soustavy lineárních rovnic, část 1](06A-2024-GEM-LinearSystems-Part1)

## Category
Mathematical Term