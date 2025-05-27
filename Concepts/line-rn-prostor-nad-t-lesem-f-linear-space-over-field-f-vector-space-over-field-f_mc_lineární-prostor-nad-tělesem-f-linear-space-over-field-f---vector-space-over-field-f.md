# Lineární prostor nad tělesem F (Linear Space over Field F / Vector Space over Field F)

## Summary
A set L (vectors) equipped with two operations: vector addition ($+: L \times L \to L$) and scalar multiplication ($\bullet: F \times L \to L$), satisfying specific axioms related to associativity, commutativity, existence of zero/opposite vectors, and distributivity involving scalars and vectors.

## Detailed Explanation
A linear space, often synonymously called a vector space, is one of the most foundational structures in linear algebra. It generalizes the concept of vectors in Euclidean space to a much broader context. It consists of a set of "vectors" and a "field" of scalars, along with two operations that must adhere to a specific set of rules (axioms).

**Definition (Source: 01B-2024-linear-spaces-over-F):** A set L (vectors) equipped with two operations: vector addition ($+: L \times L \to L$) and scalar multiplication ($\bullet: F \times L \to L$), satisfying specific axioms related to associativity, commutativity, existence of zero/opposite vectors, and distributivity involving scalars and vectors.

These axioms typically include:
1.  **Axioms for Vector Addition (L, +) forming an Abelian Group:**
    *   **Associativity:** $(\mathbf{u} + \mathbf{v}) + \mathbf{w} = \mathbf{u} + (\mathbf{v} + \mathbf{w})$ for all $\mathbf{u}, \mathbf{v}, \mathbf{w} \in L$.
    *   **Commutativity:** $\mathbf{u} + \mathbf{v} = \mathbf{v} + \mathbf{u}$ for all $\mathbf{u}, \mathbf{v} \in L$.
    *   **Existence of zero vector:** There exists a unique zero vector $\mathbf{0} \in L$ such that $\mathbf{u} + \mathbf{0} = \mathbf{u}$ for all $\mathbf{u} \in L$.
    *   **Existence of additive inverse:** For every $\mathbf{u} \in L$, there exists a vector $-\mathbf{u} \in L$ such that $\mathbf{u} + (-\mathbf{u}) = \mathbf{0}$.
2.  **Axioms for Scalar Multiplication (F, L, \bullet):**
    *   **Compatibility of scalar multiplication with field multiplication:** $a(b\mathbf{u}) = (ab)\mathbf{u}$ for all $a, b \in F$ and $\mathbf{u} \in L$.
    *   **Distributivity of scalar multiplication over vector addition:** $a(\mathbf{u} + \mathbf{v}) = a\mathbf{u} + a\mathbf{v}$ for all $a \in F$ and $\mathbf{u}, \mathbf{v} \in L$.
    *   **Distributivity of scalar multiplication over scalar addition:** $(a+b)\mathbf{u} = a\mathbf{u} + b\mathbf{u}$ for all $a, b \in F$ and $\mathbf{u} \in L$.
    *   **Identity element for scalar multiplication:** $1\mathbf{u} = \mathbf{u}$ for all $\mathbf{u} \in L$ (where 1 is the multiplicative identity in field F).

## Importance/Relevance
This concept has an overall importance score of 0.98. The linear space (vector space) is the central concept in linear algebra. It provides the framework for understanding linear transformations, eigenvalues, eigenvectors, and many other critical topics. It has vast applications in physics, engineering, computer science, economics, and many other fields.

## Connections
This concept appears in the following lectures:
*   **Lineární prostory nad F** (ID: 01B-2024-linear-spaces-over-F)

## Category
Fundamental Concept