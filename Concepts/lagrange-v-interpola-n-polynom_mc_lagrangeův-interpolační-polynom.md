# Lagrangeův interpolační polynom

## Summary
For distinct real numbers a1, ..., an and any n-tuple (b1, ..., bn), there exists a unique polynomial P(x) of degree at most n-1 such that P(ai) = bi for all i. This polynomial is called the Lagrange interpolation polynomial.

## Detailed Explanation
The **Lagrange interpolation polynomial** addresses the problem of finding a polynomial that passes through a given set of data points. Specifically, for a set of $n$ distinct real numbers $a_1, \dots, a_n$ (known as nodes or x-coordinates) and any corresponding $n$-tuple of real numbers $(b_1, \dots, b_n)$ (known as values or y-coordinates), there is a unique polynomial $P(x)$ whose degree is at most $n-1$, such that $P(a_i) = b_i$ for all $i = 1, \dots, n$.

This polynomial is a powerful tool for approximating functions or reconstructing a polynomial from a finite number of its points. The uniqueness guarantees that there's only one such polynomial for a given set of conditions.
This definition comes from the lecture "Lineární zobrazení, část 2" (ID: 05A-2024-Linear-Transformations-Part2).

## Key Aspects/Components
(No specific key aspects provided in the data.)

## Importance/Relevance
This concept has an importance score of 0.7 out of 1.0. The Lagrange interpolation polynomial is fundamental in numerical analysis, approximation theory, and scientific computing. It provides a direct method for polynomial interpolation and is used in various applications, from computer graphics to engineering.

## Connections
This concept appears in the lecture:
*   **Lineární zobrazení, část 2** (Lecture ID: 05A-2024-Linear-Transformations-Part2)

## Category
Theorem/Algorithm