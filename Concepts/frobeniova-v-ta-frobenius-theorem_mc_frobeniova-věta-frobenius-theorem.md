# Frobeniova věta (Frobenius Theorem)

## Summary
A system of linear equations $(A | b)$ has a solution if and only if the rank of the coefficient matrix $A$ is equal to the rank of the augmented matrix $(A | b)$.

## Detailed Explanation
The Frobenius Theorem, also known as the Rouché–Capelli theorem in some contexts, is a fundamental theorem in linear algebra that provides a necessary and sufficient condition for a system of linear equations to have at least one solution. It establishes a direct link between the existence of solutions and the ranks of specific matrices derived from the system.

*   **Theorem Statement:** A system of linear equations $(A | b)$ has a solution if and only if the rank of the coefficient matrix $A$ is equal to the rank of the augmented matrix $(A | b)$. (Source: 06A-2024-GEM-LinearSystems-Part1)

In simpler terms, if adding the constant vector $b$ as an extra column to the coefficient matrix $A$ does not increase the number of linearly independent rows (or columns), then the system is consistent (i.e., has a solution). If the rank of the augmented matrix is greater than the rank of the coefficient matrix, it implies that the vector $b$ is linearly independent of the columns of $A$, meaning $b$ cannot be expressed as a linear combination of the columns of $A$, and thus no solution exists.

## Importance/Relevance
This theorem is of paramount importance because it provides a clear and computationally verifiable criterion for the solvability of any system of linear equations. It is a cornerstone in the theory of linear systems and is widely applied in various fields of mathematics, science, and engineering to determine the feasibility of solutions. This concept has an exceptionally high importance score of 0.95.

## Connections
This concept appears in the lecture:
*   "GEM a soustavy lineárních rovnic, část 1" (Lecture ID: 06A-2024-GEM-LinearSystems-Part1)

## Category
Theorem