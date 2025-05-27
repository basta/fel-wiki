# Gaussova eliminace (Gaussian Elimination)

## Summary
A method used to solve systems of linear equations or to find the inverse of a matrix, often used in a block form for finding transformation matrices.

## Detailed Explanation
**Gaussian elimination** is a fundamental algorithm in linear algebra used for solving systems of linear equations and for finding the inverse of a matrix. The method involves applying a sequence of elementary row operations to a matrix until it is in row echelon form or reduced row echelon form.

### Definitions
*   **Definition 1 (from lec-coordinate-transformation-matrices-05B-2024):** A method used to solve systems of linear equations or to find the inverse of a matrix, often used in a block form for finding transformation matrices.

When solving systems of equations, the augmented matrix representing the system is transformed into an upper triangular form, from which the solution can be found by back-substitution. For finding the inverse of a matrix, the identity matrix is augmented to the original matrix, and Gaussian elimination is applied to transform the original matrix into the identity, resulting in the inverse matrix on the augmented side. This technique is also valuable in a block form for more complex operations, such as deriving transformation matrices.

## Importance/Relevance
This algorithm is of moderate importance due to its foundational role in computational linear algebra. It provides a systematic and efficient approach to solving common problems, serves as a building block for more complex matrix operations, and is widely used in various scientific and engineering fields.

## Connections
### Appears in Lectures
*   [Transformace souřadnic](lec-coordinate-transformation-matrices-05B-2024)

### Category
Algorithm