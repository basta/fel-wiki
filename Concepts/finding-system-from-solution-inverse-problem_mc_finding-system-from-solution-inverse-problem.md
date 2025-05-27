# Finding System from Solution (Inverse Problem)

## Summary
The process of constructing a linear system $A * x = b$ given its solution as an affine subspace. This involves using the spanning vectors to define the null space of $A$ and the particular solution to determine $b$.

## Detailed Explanation
Typically, one is given a linear system $A * x = b$ and asked to find its solution. The "Finding System from Solution" problem, or inverse problem, reverses this. We are given the solution (often in the form of an affine subspace) and must deduce the original matrix $A$ and vector $b$.

**Definition:**
The process of constructing a linear system $A * x = b$ given its solution as an affine subspace. This involves using the spanning vectors to define the null space of $A$ and the particular solution to determine $b$. (Source: 06B-2024-GEM-souostavy-cast2)

If the solution is given as $x = p + c_1 v_1 + \dots + c_k v_k$, where $p$ is a particular solution and $v_1, \dots, v_k$ are the basis vectors for the null space of $A$:
1.  **Determine A:** Since $v_1, \dots, v_k$ span the null space of $A$, it means that $A * v_i = o$ for each $i$. This implies that $A$ must be orthogonal to each $v_i$. This property can be used to construct the rows of $A$ (which are orthogonal to the null space vectors). Essentially, the rows of $A$ will be in the orthogonal complement of the span of $v_1, \dots, v_k$.
2.  **Determine b:** Once $A$ is found, the vector $b$ can be determined by applying $A$ to the particular solution $p$: $b = A * p$.

This inverse problem highlights a deeper understanding of the relationship between a linear system and its solution space.

## Importance/Relevance
This methodology is of high importance as it tests a comprehensive understanding of linear systems, null spaces, and affine subspaces. It demonstrates the ability to not only solve systems but also to reconstruct them from their fundamental properties, which is crucial in various engineering and scientific applications where system models need to be inferred from observed behaviors.

## Connections
This concept appears in the following lecture:
*   "GEM a soustavy lineárních rovnic, část 2" (ID: 06B-2024-GEM-souostavy-cast2)

## Category
Methodology