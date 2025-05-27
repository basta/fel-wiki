# Hodnost matice (Rank of a matrix)

## Summary
The maximum number of linearly independent row or column vectors in a matrix. It is equal to the number of non-zero rows in its upper block form after Gaussian elimination.

## Detailed Explanation
The rank of a matrix is a crucial property in linear algebra that quantifies its "degeneracy" or the "number of dimensions" spanned by its rows or columns. It is formally defined as the maximum number of linearly independent row vectors, which is always equal to the maximum number of linearly independent column vectors.

A practical way to determine the rank is by performing Gaussian elimination on the matrix. Once the matrix is transformed into its row echelon form (or upper block form), the rank is simply the count of non-zero rows.

*   **Definition:** The maximum number of linearly independent row or column vectors in a matrix. It is equal to the number of non-zero rows in its upper block form after Gaussian elimination. (Source: 06A-2024-GEM-LinearSystems-Part1)

## Importance/Relevance
The rank of a matrix is a fundamental concept used to determine the solvability of linear systems, the dimension of the column space and null space, and properties of linear transformations. It plays a central role in numerous applications, including optimization, statistics, and engineering. This concept has a high importance score of 0.8.

## Connections
This concept appears in the lecture:
*   "GEM a soustavy lineárních rovnic, část 1" (Lecture ID: 06A-2024-GEM-LinearSystems-Part1)

## Category
Mathematical Property