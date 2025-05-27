# Diagonální matice

## Summary

A Diagonal Matrix is a square matrix in which all elements outside the main diagonal are zero.

## Detailed Explanation

Diagonal matrices are among the simplest and most well-behaved types of matrices in linear algebra. Their simple structure makes them very useful in various calculations and theoretical considerations.

**Definition:**
*   A matrix where all entries outside the main diagonal are zero. This definition comes from the lecture "Jordanův tvar".

In a diagonal matrix $D$, the only non-zero entries $d_{ij}$ occur when $i=j$. For example:
$$
D = \begin{pmatrix}
d_1 & 0 & 0 \\
0 & d_2 & 0 \\
0 & 0 & d_3
\end{pmatrix}
$$
Operations with diagonal matrices are straightforward:
*   Adding two diagonal matrices results in a diagonal matrix.
*   Multiplying two diagonal matrices results in a diagonal matrix (their diagonal entries are multiplied).
*   Inverting a diagonal matrix (if possible) results in a diagonal matrix where each diagonal entry is the reciprocal of the original.

## Importance

With an overall importance score of 0.6, Diagonal Matrices are a moderately important foundational concept in linear algebra. They simplify many matrix operations and are crucial for understanding concepts like eigenvalues, eigenvectors, and diagonalization of matrices.

## Connections

This concept is discussed in the lecture series titled "Jordanův tvar".

## Category

This concept is categorized as a **Mathematical Object**.
