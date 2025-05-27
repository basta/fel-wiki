# Řádkové elementární úpravy (Elementary row operations)

## Summary
Three types of operations that can be performed on the rows of a matrix: (I) adding a scalar multiple of one row to another, (II) swapping two rows, and (III) multiplying a row by a non-zero scalar.

## Detailed Explanation
Elementary row operations are crucial manipulations performed on the rows of a matrix. These operations are fundamental because they do not change the solution set of a system of linear equations represented by the matrix. They are the building blocks for algorithms like [Gaussian Elimination](#mc_gaussova-eliminační-metoda-gem) to transform a matrix into a simpler form, such as [row echelon form](#mc_horní-blokový-tvar-matice-upper-block-form-matrix).

*   **Definition:** Three types of operations that can be performed on the rows of a matrix: (I) adding a scalar multiple of one row to another, (II) swapping two rows, and (III) multiplying a row by a non-zero scalar. (Source: 06A-2024-GEM-LinearSystems-Part1)

## Key Aspects
There are precisely three types of elementary row operations:
1.  **Type I: Swapping two rows ($R_i \leftrightarrow R_j$)**
    *   This operation involves interchanging the positions of any two rows.
    *   Example: Swapping Row 1 and Row 2.
2.  **Type II: Multiplying a row by a non-zero scalar ($k R_i \to R_i$, where $k \neq 0$)**
    *   Each element in a specific row is multiplied by a non-zero constant.
    *   Example: Multiplying all elements in Row 3 by 2.
3.  **Type III: Adding a scalar multiple of one row to another ($R_i + k R_j \to R_i$)**
    *   A row is replaced by the sum of itself and a scalar multiple of another row.
    *   Example: Adding 3 times Row 1 to Row 2.

These operations are reversible and form the basis for reducing matrices to simpler, equivalent forms.

## Importance
This concept is of *very high importance* (score: 0.9) as elementary row operations are the fundamental tools for matrix manipulation, indispensable for solving linear systems, finding inverses of matrices, and determining the rank of a matrix.

## Connections
This concept appears in the following lectures:
*   [GEM a soustavy lineárních rovnic, část 1](06A-2024-GEM-LinearSystems-Part1)

## Category
Method Step