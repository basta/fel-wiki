# Linearita výpočtu souřadnic

## Summary
For any finite ordered basis B of a linear space L, the mapping from a vector x to its coordinates coordB(x) is linear. This means that for any vectors x, y in L and scalar a, the following properties hold: 1) coordB(x + y) = coordB(x) + coordB(y) and 2) coordB(a · x) = a · coordB(x).

## Detailed Explanation
The linearity of coordinate computation is a crucial property that ensures consistency between vector space operations and their coordinate representations. It implies that operations like vector addition and scalar multiplication can be performed directly on the coordinate vectors themselves, and the result will accurately correspond to the coordinates of the sum or scalar multiple of the original vectors.

### Definition:
For any finite ordered basis $B$ of a linear space $L$, the mapping from a vector $x$ to its coordinates $coord_B(x)$ is linear. This means that for any vectors $x, y$ in $L$ and scalar $a$, the following properties hold:
1.  $coord_B(x + y) = coord_B(x) + coord_B(y)$
2.  $coord_B(a \cdot x) = a \cdot coord_B(x)$

## Importance/Relevance
This concept is highly important (overall importance score of 0.9) because it establishes that the coordinate mapping is a linear isomorphism between the vector space and the coordinate space $F^n$. This linearity is fundamental for converting abstract vector space problems into concrete matrix problems, significantly simplifying calculations and enabling the extensive use of linear algebra tools.

## Connections

### Appears In Lectures:
*   Souřadnice vzhledem k uspořádané bázi a komutativní diagramy

## Category
Theorem/Property