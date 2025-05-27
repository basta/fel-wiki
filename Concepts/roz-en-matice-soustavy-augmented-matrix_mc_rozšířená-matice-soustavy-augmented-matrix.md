# Rozšířená matice soustavy (Augmented matrix)

## Summary
A matrix obtained by appending the columns of two given matrices, usually to represent the coefficients and constant terms of a system of linear equations.

## Detailed Explanation
The augmented matrix is a fundamental concept in linear algebra, particularly when solving systems of linear equations. It combines the coefficient matrix of a system with the column vector of constant terms into a single matrix. This unified representation simplifies the process of applying row operations to solve the system.

*   **Definition:** A matrix obtained by appending the columns of two given matrices, usually to represent the coefficients and constant terms of a system of linear equations. (Source: 06A-2024-GEM-LinearSystems-Part1)

For a system of linear equations like:
$$
a_{11}x_1 + a_{12}x_2 + \dots + a_{1n}x_n = b_1 \\
a_{21}x_1 + a_{22}x_2 + \dots + a_{2n}x_n = b_2 \\
\vdots \\
a_{m1}x_1 + a_{m2}x_2 + \dots + a_{mn}x_n = b_m
$$
The augmented matrix would be:
$$
\begin{pmatrix}
a_{11} & a_{12} & \dots & a_{1n} & | & b_1 \\
a_{21} & a_{22} & \dots & a_{2n} & | & b_2 \\
\vdots & \vdots & \ddots & \vdots & | & \vdots \\
a_{m1} & a_{m2} & \dots & a_{mn} & | & b_m
\end{pmatrix}
$$

## Importance
This concept holds *high importance* (score: 0.8) as it provides a compact and standardized way to represent linear systems, which is crucial for algorithmic solutions like Gaussian elimination.

## Connections
This concept appears in the following lectures:
*   [GEM a soustavy lineárních rovnic, část 1](06A-2024-GEM-LinearSystems-Part1)

## Category
Mathematical Term