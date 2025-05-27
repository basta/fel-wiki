# Regulární matice (Regular matrix)

## Summary
A square matrix $A$ is defined as **regular** (or invertible, or non-singular) if and only if its determinant is non-zero, i.e., $\text{det}(A) \neq 0$. For such matrices, its inverse $A^{-1}$ exists and can be computed using the formula $A^{-1} = \frac{1}{\text{det}(A)} \text{adj}(A)$.

## Detailed Explanation
The concept of a regular matrix is central to linear algebra and has profound implications for solving systems of linear equations, understanding linear transformations, and many other matrix operations.

A square matrix $A$ of size $n \times n$ is called **regular** if it satisfies any of the following equivalent conditions:

*   **Non-zero Determinant:** The determinant of $A$ is not zero: $\text{det}(A) \neq 0$. This is the most common and practical definition.
*   **Existence of Inverse:** There exists an $n \times n$ matrix $A^{-1}$ such that $A A^{-1} = A^{-1} A = I_n$, where $I_n$ is the $n \times n$ identity matrix. This matrix $A^{-1}$ is unique and called the inverse of $A$.
*   **Unique Solution to Homogeneous System:** The homogeneous system of linear equations $A\mathbf{x} = \mathbf{0}$ has only the trivial solution $\mathbf{x} = \mathbf{0}$.
*   **Linearly Independent Columns/Rows:** The columns (or rows) of $A$ are linearly independent vectors.
*   **Full Rank:** The rank of matrix $A$ is $n$ (its maximum possible rank).
*   **Isomorphic Linear Transformation:** The linear transformation represented by $A$ is an isomorphism (a bijective mapping).

The formula for computing the inverse of a regular matrix $A$ is directly related to its determinant and its adjoint matrix:
$$ A^{-1} = \frac{1}{\text{det}(A)} \text{adj}(A) $$
If $\text{det}(A) = 0$, the matrix is called **singular** (or non-regular), and its inverse does not exist. Singular matrices indicate that the associated linear transformation is not injective or surjective, meaning it maps multiple vectors to the same output or does not cover the entire output space.

## Key Aspects/Components
*   **Determinant Condition:** The determinant being non-zero is the defining characteristic.
*   **Invertibility:** Regular matrices are precisely those matrices that possess an inverse.
*   **Solution of Linear Systems:** Regular matrices guarantee a unique solution for systems of the form $A\mathbf{x} = \mathbf{b}$.

## Importance/Relevance
Regular matrices are highly important in linear algebra and its applications, with an overall importance score of 0.9. They are essential for solving linear systems, performing coordinate transformations, and understanding the properties of vector spaces and linear mappings.

## Connections
This concept appears in:
*   Lecture: "Determinant, část 2" (`07B-2024-L2`)
*   Lecture: "Transformace souřadnic" (`lec-coordinate-transformation-matrices-05B-2024`)

## Category
Property/Condition