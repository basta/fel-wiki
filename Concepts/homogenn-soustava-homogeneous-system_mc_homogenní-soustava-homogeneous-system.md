# Homogenní soustava (Homogeneous system)

## Summary
A system of linear equations of the form $A x = o$, where $o$ is the zero vector.

## Detailed Explanation
A homogeneous system of linear equations is a special type of linear system where all the constant terms are zero. This means that the right-hand side of every equation in the system is zero.

*   **Definition:** A system of linear equations of the form $A x = o$, where $o$ is the zero vector. (Source: 06A-2024-GEM-LinearSystems-Part1)

For example, if we have a system of three equations with three unknowns:
$a_{11}x_1 + a_{12}x_2 + a_{13}x_3 = 0$
$a_{21}x_1 + a_{22}x_2 + a_{23}x_3 = 0$
$a_{31}x_1 + a_{32}x_2 + a_{33}x_3 = 0$

This can be written in matrix form as $A x = o$, where $A$ is the coefficient matrix, $x$ is the vector of unknowns, and $o$ is the zero vector (a vector of all zeros).

A key property of homogeneous systems is that they always have at least one solution, namely the trivial solution where all unknowns are zero ($x = o$). This is because $A o = o$ is always true. The existence of non-trivial solutions depends on the rank of the matrix $A$: non-trivial solutions exist if and only if the rank of $A$ is less than the number of unknowns.

## Importance/Relevance
Homogeneous systems are crucial in linear algebra because their solution set forms a vector space (the null space or kernel of the matrix $A$). Understanding their solutions is essential for comprehending the structure of general linear systems (non-homogeneous systems), as the general solution to $A x = b$ is the sum of a particular solution to $A x = b$ and the general solution to the associated homogeneous system $A x = o$. This concept has an importance score of 0.7.

## Connections
This concept appears in the lecture:
*   "GEM a soustavy lineárních rovnic, část 1" (Lecture ID: 06A-2024-GEM-LinearSystems-Part1)

## Category
System Type