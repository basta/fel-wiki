# Affine Subspace

## Summary
A set of points represented as $p + \text{span}(x_1,...,x_D)$, where $p$ is a particular vector and $x_1,...,x_D$ are linearly independent vectors spanning the 'direction' or 'orientation' of the subspace. It represents the general solution set of a linear system.

## Detailed Explanation
In linear algebra, an affine subspace is a generalization of a linear subspace that does not necessarily pass through the origin. It can be thought of as a linear subspace that has been "shifted" by a vector.

**Definition:**
A set of points represented as $p + \text{span}(x_1,...,x_D)$, where $p$ is a particular vector and $x_1,...,x_D$ are linearly independent vectors spanning the 'direction' or 'orientation' of the subspace. It represents the general solution set of a linear system. (Source: 06B-2024-GEM-souostavy-cast2)

Here:
*   $p$ is any particular solution to the non-homogeneous linear system $A * x = b$.
*   $\text{span}(x_1,...,x_D)$ represents the solution space of the corresponding homogeneous system $A * x = o$, which is a linear subspace (also known as the null space or kernel of A). The vectors $x_1,...,x_D$ form a basis for this null space.

The combination $p + \text{span}(x_1,...,x_D)$ signifies that any solution to the non-homogeneous system can be expressed as the sum of a particular solution and a solution to the homogeneous system.

## Importance/Relevance
This concept is of very high importance as it precisely describes the structure of the solution set for any consistent system of linear equations. Understanding affine subspaces is crucial for comprehending the complete nature of solutions, especially when they are not unique.

## Connections
This concept appears in the following lecture:
*   "GEM a soustavy lineárních rovnic, část 2" (ID: 06B-2024-GEM-souostavy-cast2)

## Category
Definition