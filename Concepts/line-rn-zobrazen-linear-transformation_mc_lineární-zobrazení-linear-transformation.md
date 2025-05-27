# Lineární zobrazení (Linear Transformation)

## Summary
A function between vector spaces that preserves vector addition and scalar multiplication.

## Detailed Explanation
A **Linear Transformation** (also known as a linear map or linear operator) is a special kind of function that maps vectors from one vector space to another, while preserving the fundamental operations of vector addition and scalar multiplication.

According to definition:
*   "A function between vector spaces that preserves vector addition and scalar multiplication." (Source: lec-coordinate-transformation-matrices-05B-2024)

For a function $L: V \to W$ to be a linear transformation, where $V$ and $W$ are vector spaces over the same field, it must satisfy two conditions for all vectors $\mathbf{u}, \mathbf{v}$ in $V$ and all scalars $c$:
1.  **Additivity:** $L(\mathbf{u} + \mathbf{v}) = L(\mathbf{u}) + L(\mathbf{v})$
2.  **Homogeneity of degree 1:** $L(c\mathbf{u}) = cL(\mathbf{u})$

These two properties ensure that the algebraic structure of the vector space is maintained under the transformation. Linear transformations are widely used in mathematics, physics, engineering, and computer graphics to model various phenomena such as rotations, reflections, scaling, and projections.

## Importance/Relevance
This is a fundamental concept (score 0.8) in linear algebra, providing the backbone for understanding how vector spaces relate to each other and for defining matrix operations.

## Connections
This concept appears in the following lecture:
*   "Transformace souřadnic" (Lecture ID: lec-coordinate-transformation-matrices-05B-2024)

## Category
Fundamental Concept