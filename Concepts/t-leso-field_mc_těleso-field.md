# Těleso (Field)

## Summary
A collection of objects (elements of the field F) that can be added and multiplied, satisfying specific algebraic properties analogous to real numbers (existence of zero/identity, associativity, commutativity, distributivity, existence of inverses for addition and non-zero elements for multiplication).

## Detailed Explanation
A field, denoted typically by $F$, is a set along with two operations, usually called addition ($+$) and multiplication ($\cdot$), that satisfy the following axioms:
1.  **Closure:** For all $a, b \in F$, $a+b \in F$ and $a \cdot b \in F$.
2.  **Associativity:** For all $a, b, c \in F$, $(a+b)+c = a+(b+c)$ and $(a \cdot b) \cdot c = a \cdot (b \cdot c)$.
3.  **Commutativity:** For all $a, b \in F$, $a+b = b+a$ and $a \cdot b = b \cdot a$.
4.  **Identity Elements:** There exists an additive identity (zero element) $0 \in F$ such that for all $a \in F$, $a+0 = a$. There exists a multiplicative identity (unity element) $1 \in F$ such that for all $a \in F$, $a \cdot 1 = a$. Also, $0 \ne 1$.
5.  **Inverse Elements:** For every $a \in F$, there exists an additive inverse $-a \in F$ such that $a+(-a) = 0$. For every $a \in F$ where $a \ne 0$, there exists a multiplicative inverse $a^{-1} \in F$ such that $a \cdot a^{-1} = 1$.
6.  **Distributivity:** For all $a, b, c \in F$, $a \cdot (b+c) = (a \cdot b) + (a \cdot c)$.

Common examples of fields include the set of real numbers ($\mathbb{R}$), rational numbers ($\mathbb{Q}$), and complex numbers ($\mathbb{C}$). Finite fields also exist, such as $\mathbb{Z}_p$ for a prime number $p$. Fields are crucial because they provide the set of scalars over which vector spaces are defined.

### Definitions
*   **Definition from Lecture "Lineární prostory nad F" (ID: 01B-2024-linear-spaces-over-F):**
    "A collection of objects (elements of the field F) that can be added and multiplied, satisfying specific algebraic properties analogous to real numbers (existence of zero/identity, associativity, commutativity, distributivity, existence of inverses for addition and non-zero elements for multiplication)."

## Importance/Relevance
With an exceptionally high importance score of 0.95, the concept of a "Field" is paramount in abstract algebra and linear algebra. Fields provide the scalar domain for vector spaces, meaning all vector space operations (vector addition and scalar multiplication) are defined with respect to a specific field. Understanding fields is prerequisite to understanding vector spaces, modules, and many other higher-level algebraic structures.

## Connections
This concept appears in the following lectures:
*   [Lineární prostory nad F](01B-2024-linear-spaces-over-F)
*   [Lineární prostory nad R](linear_spaces_over_R_lec01)

## Category
Algebraic Structure