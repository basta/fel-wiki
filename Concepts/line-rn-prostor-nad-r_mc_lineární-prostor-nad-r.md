# Lineární prostor (nad R)

## Summary
A linear space (or vector space) over the real numbers $\mathbb{R}$ is a set $L$ equipped with two binary operations: vector addition ($+: L \times L \rightarrow L$) and scalar multiplication ($\cdot: \mathbb{R} \times L \rightarrow L$). These operations must satisfy eight specific axioms, which define properties of addition (commutativity, associativity, existence of zero vector and opposite vector) and scalar multiplication (associativity, identity element), and distributive laws.

## Detailed Explanation
The concept of a linear space is central to linear algebra. It generalizes the properties of vectors in two or three-dimensional Euclidean space to abstract sets of "vectors." The "nad R" (over $\mathbb{R}$) signifies that the scalars used for multiplication are real numbers.

**Definition:**
*   From Lecture "Lineární prostory nad R" (`linear_spaces_over_R_lec01`):
    A set $L$ together with two functions (vector addition $+: L \times L \rightarrow L$ and scalar multiplication $\cdot: \mathbb{R} \times L \rightarrow L$) satisfying eight axioms (properties of addition and scalar multiplication, distributive laws).

These eight axioms are typically:
### Axioms of Vector Addition:
1.  **Commutativity:** $x + y = y + x$ for all $x, y \in L$.
2.  **Associativity:** $(x + y) + z = x + (y + z)$ for all $x, y, z \in L$.
3.  **Existence of Zero Vector:** There exists a zero vector $o \in L$ such that $x + o = x$ for all $x \in L$.
4.  **Existence of Opposite Vector:** For every $x \in L$, there exists an opposite vector $-x \in L$ such that $x + (-x) = o$.

### Axioms of Scalar Multiplication:
5.  **Associativity of Scalar Multiplication:** $a \cdot (b \cdot x) = (a \cdot b) \cdot x$ for all $a, b \in \mathbb{R}$ and $x \in L$.
6.  **Multiplicative Identity:** $1 \cdot x = x$ for all $x \in L$, where $1$ is the multiplicative identity in $\mathbb{R}$.

### Axioms of Distributivity:
7.  **Distributivity of Scalar Multiplication over Vector Addition:** $a \cdot (x + y) = a \cdot x + a \cdot y$ for all $a \in \mathbb{R}$ and $x, y \in L$.
8.  **Distributivity of Scalar Multiplication over Scalar Addition:** $(a + b) \cdot x = a \cdot x + b \cdot x$ for all $a, b \in \mathbb{R}$ and $x \in L$.

## Importance/Relevance
With an `overallImportanceScore` of 1.0, "Lineární prostor (nad R)" is a critically important, core definition in linear algebra. It provides the foundational structure upon which almost all other concepts in the field are built, including linear transformations, subspaces, bases, dimensions, eigenvalues, and eigenvectors. Understanding these axioms is key to recognizing what constitutes a valid vector space and applying linear algebraic principles to various mathematical and real-world problems.

## Connections
This concept appears in the following lecture:
*   [Lineární prostory nad R](linear_spaces_over_R_lec01)

## Category
Core Definition