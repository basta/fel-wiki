# Matice transformace souřadnic (Coordinate Transformation Matrix)

## Summary
A matrix $T_{B \to C}$ that transforms coordinates of a vector from basis B to basis C. Its j-th column is the coordinate representation of the j-th basis vector from B in basis C.

## Detailed Explanation
A **Coordinate Transformation Matrix**, often denoted as $T_{B \to C}$, is a special type of matrix used to convert the coordinate representation of a vector from one basis (Basis B) to another basis (Basis C).

According to definition:
*   "A matrix T_B->C that transforms coordinates of a vector from basis B to basis C. Its j-th column is the coordinate representation of the j-th basis vector from B in basis C." (Source: lec-coordinate-transformation-matrices-05B-2024)

This matrix is constructed by taking each basis vector from the original basis (B) and expressing it as a linear combination of the vectors in the new basis (C). These coordinate representations then form the columns of the transformation matrix. If $[\mathbf{v}]_B$ are the coordinates of a vector $\mathbf{v}$ in basis B, then the coordinates of the same vector in basis C, $[\mathbf{v}]_C$, can be found by multiplying: $[\mathbf{v}]_C = T_{B \to C} [\mathbf{v}]_B$.

## Importance/Relevance
This is a highly fundamental and important concept (score 0.95) in linear algebra, essential for understanding how vectors are represented in different coordinate systems and for performing changes of basis.

## Connections
This concept appears in the following lecture:
*   "Transformace souřadnic" (Lecture ID: lec-coordinate-transformation-matrices-05B-2024)

## Category
Core Concept