# Pseudoinverse (Moore-Penrose inverse)

## Summary
For any matrix $A$, there exists a unique pseudoinverse $A^+$ satisfying the four Moore-Penrose conditions: $AA^+A = A$, $A^+AA^+ = A^+$, $(A^+A)^T = A^+A$, and $(AA^+)^T = AA^+$. It extends the concept of an inverse to non-square or singular matrices.

## Detailed Explanation
*   For any matrix $A$, there exists a unique pseudoinverse $A^+$ satisfying the four Moore-Penrose conditions: $AA^+A = A$, $A^+AA^+ = A^+$, $(A^+A)^T = A^+A$, and $(AA^+)^T = AA^+$. It extends the concept of an inverse to non-square or singular matrices. (Source: svd-pseudoinverse-lecture)
*   The pseudoinverse of a matrix $A$ with SVD $A=USV^T$ is $A^+ = VS^+U^T$, where $S^+$ is obtained by taking the reciprocal of non-zero singular values on the diagonal of $S$ and transposing (or using zeroes for zero singular values). (Source: svd-pseudoinverse-lecture)

## Importance/Relevance
This concept holds an importance score of 9.0/10.

## Connections
*   **Appears in Lectures:**
    *   [SVD rozklad a pseudoinverse](./svd-pseudoinverse-lecture)
*   **Aliases:** None

## Category
Mathematical Operation