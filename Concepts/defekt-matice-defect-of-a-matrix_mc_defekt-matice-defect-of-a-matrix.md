# Defekt matice (Defect of a matrix)

## Summary
The number of columns of a matrix minus its rank. For a system $A x = b$ with $s$ unknowns, the defect of matrix $A$ is $d = s - \text{rank}(A)$.

## Detailed Explanation
The defect of a matrix, also known as its nullity, is a measure related to the size of its null space. It quantifies how many "free variables" or "parameters" are present in the general solution to a homogeneous system of linear equations involving that matrix.

Formally, the defect is calculated by subtracting the rank of the matrix from its total number of columns. This is directly linked to the Rank-Nullity Theorem, which states that for an $m \times n$ matrix $A$, $\text{rank}(A) + \text{nullity}(A) = n$.

*   **Definition:** The number of columns of a matrix minus its rank. For a system $A x = b$ with $s$ unknowns, the defect of matrix $A$ is $d = s - \text{rank}(A)$. (Source: 06A-2024-GEM-LinearSystems-Part1)

This definition highlights its direct connection to the number of unknowns in a system and the rank of the coefficient matrix.

## Importance/Relevance
The defect is crucial for understanding the structure of solution sets for linear systems, particularly homogeneous ones. It directly relates to the dimension of the null space (kernel) of a linear transformation represented by the matrix, and through the Rank-Nullity Theorem, it connects the dimension of the domain, the rank, and the defect. This concept has an importance score of 0.75.

## Connections
This concept appears in the lecture:
*   "GEM a soustavy lineárních rovnic, část 1" (Lecture ID: 06A-2024-GEM-LinearSystems-Part1)

## Category
Mathematical Property