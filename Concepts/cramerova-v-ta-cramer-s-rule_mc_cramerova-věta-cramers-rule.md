# Cramerova věta (Cramer's Rule)

## Summary
Cramer's Rule is a formula that provides a direct method for finding the unique solution to a system of linear equations $A\mathbf{x} = \mathbf{b}$, provided that the coefficient matrix $A$ is square and regular (i.e., $\text{det}(A) \neq 0$). The $j$-th component of the solution vector $\mathbf{x}$ is given by the ratio of two determinants: $x_j = \frac{\text{det}(A_j)}{\text{det}(A)}$, where $A_j$ is the matrix formed by replacing the $j$-th column of $A$ with the constant vector $\mathbf{b}$.

## Detailed Explanation
Cramer's Rule is a powerful theorem in linear algebra that offers an explicit formula for the components of the solution vector of a system of linear equations. While it can be computationally intensive for large systems compared to methods like Gaussian elimination, it provides a clear theoretical understanding of the solution structure and is often used for smaller systems or for deriving other theoretical results.

Consider a system of $n$ linear equations in $n$ variables, represented in matrix form as $A\mathbf{x} = \mathbf{b}$:
$$ A\mathbf{x} = \begin{pmatrix}
a_{11} & a_{12} & \dots & a_{1n} \\
a_{21} & a_{22} & \dots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \dots & a_{nn}
\end{pmatrix}
\begin{pmatrix}
x_1 \\
x_2 \\
\vdots \\
x_n
\end{pmatrix}
=
\begin{pmatrix}
b_1 \\
b_2 \\
\vdots \\
b_n
\end{pmatrix} = \mathbf{b} $$

Cramer's Rule states that if the coefficient matrix $A$ is square and regular (meaning its determinant $\text{det}(A) \neq 0$), then the system has a unique solution $\mathbf{x} = (x_1, x_2, \dots, x_n)^T$, where each component $x_j$ is given by:
$$ x_j = \frac{\text{det}(A_j)}{\text{det}(A)} $$

Here:
*   $\text{det}(A)$ is the determinant of the original coefficient matrix $A$.
*   $A_j$ is a modified matrix formed by taking the original matrix $A$ and replacing its $j$-th column with the constant vector $\mathbf{b}$ (the right-hand side of the system).

In essence, to find $x_j$, one calculates the determinant of a matrix where the column corresponding to $x_j$ has been substituted by the constant vector, and then divides this by the determinant of the original coefficient matrix.

## Key Aspects/Components
*   **Applicability:** Cramer's Rule is strictly applicable only to systems of linear equations where the number of equations equals the number of variables, and the coefficient matrix is regular (non-singular).
*   **Determinant Ratios:** The rule expresses each unknown variable as a ratio of two determinants.
*   **Matrix $A_j$ Construction:** The ability to correctly construct the $A_j$ matrix by substituting the appropriate column with the constant vector $\mathbf{b}$ is key.

## Importance/Relevance
Cramer's Rule is a highly important theorem/algorithm in linear algebra (overall importance score 0.95) for its explicit and direct formulation of the solution to linear systems. While not the most efficient for practical computation with large matrices, it is invaluable for theoretical analysis and for deriving other mathematical results.

## Connections
This concept appears in:
*   Lecture: "Determinant, část 2" (`07B-2024-L2`)

## Category
Theorem/Algorithm