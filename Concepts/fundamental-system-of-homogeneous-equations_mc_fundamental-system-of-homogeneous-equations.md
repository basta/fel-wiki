# Fundamental System (of homogeneous equations)

## Summary
A set of linearly independent vectors that form a basis for the null space (kernel) of a matrix, spanning the solution space of the corresponding homogeneous linear system ($A * x = o$).

## Detailed Explanation
For a homogeneous system of linear equations $A * x = o$, where $o$ is the zero vector, the solution set always forms a vector subspace. A fundamental system is a set of vectors that "spans" this entire solution space with the smallest possible number of vectors.

**Definition:**
A set of linearly independent vectors that form a basis for the null space (kernel) of a matrix, spanning the solution space of the corresponding homogeneous linear system ($A * x = o$). (Source: 06B-2024-GEM-souostavy-cast2)

The null space of a matrix $A$ (also called the kernel of $A$, denoted $\text{Null}(A)$ or $\text{Ker}(A)$) is the set of all vectors $x$ such that $A * x = o$. This is a vector space, and a fundamental system is essentially a basis for this vector space.

The number of vectors in a fundamental system is equal to the nullity of the matrix $A$, which is given by $n - \text{rank}(A)$, where $n$ is the number of columns in $A$. These vectors are crucial for constructing the general solution of a non-homogeneous system, as the homogeneous solution component of an affine subspace is formed by the span of these fundamental system vectors.

## Importance/Relevance
This concept is of high importance as it provides the building blocks for understanding the structure of solutions to homogeneous linear systems, and by extension, the general solution of non-homogeneous systems. It is fundamental to understanding null spaces and the properties of linear transformations.

## Connections
This concept appears in the following lecture:
*   "GEM a soustavy lineárních rovnic, část 2" (ID: 06B-2024-GEM-souostavy-cast2)

## Category
Definition