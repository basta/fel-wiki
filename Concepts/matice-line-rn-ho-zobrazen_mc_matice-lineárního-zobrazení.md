# Matice lineárního zobrazení

## Summary
Given bases B and C for L1 and L2 respectively, the matrix Af of a linear transformation f: L1 -> L2 satisfies Af ⋅ coordB(x) = coordC(f(x)) for any vector x.

## Detailed Explanation
The **matrix of a linear transformation** provides a concrete representation of an abstract linear mapping between vector spaces. For a linear transformation $f: L_1 \rightarrow L_2$, where $L_1$ and $L_2$ are vector spaces, we can define a matrix $A_f$ provided we have chosen bases for these spaces.
Let $B$ be a basis for $L_1$ and $C$ be a basis for $L_2$. The matrix $A_f$ is then defined such that for any vector $x \in L_1$, the following relationship holds:
$$ A_f \cdot \text{coord}_B(x) = \text{coord}_C(f(x)) $$
Here, $\text{coord}_B(x)$ represents the coordinate vector of $x$ with respect to basis $B$, and $\text{coord}_C(f(x))$ represents the coordinate vector of $f(x)$ with respect to basis $C$. This means that multiplying the coordinate vector of $x$ in basis $B$ by the matrix $A_f$ yields the coordinate vector of the transformed vector $f(x)$ in basis $C$.
This definition comes from the lecture "Lineární zobrazení, část 2" (ID: 05A-2024-Linear-Transformations-Part2).

## Key Aspects/Components
(No specific key aspects provided in the data.)

## Importance/Relevance
This concept has a very high importance score of 0.9 out of 1.0. It is a cornerstone of linear algebra, bridging the abstract world of linear transformations with the concrete world of matrices. It allows for computations, analysis, and practical applications of linear transformations using matrix algebra.

## Connections
This concept appears in the lecture:
*   **Lineární zobrazení, část 2** (Lecture ID: 05A-2024-Linear-Transformations-Part2)

## Category
Representation