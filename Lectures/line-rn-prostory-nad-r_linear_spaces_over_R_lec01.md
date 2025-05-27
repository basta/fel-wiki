# Lineární prostory nad R
## Lineární algebra - Lecture 1

This lecture, presented by Jiří Velebil, serves as a foundational introduction to the concept of [linear spaces](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-r_mc_line-rn-prostor-nad-r) (also known as vector spaces) over the field of real numbers, R. It systematically builds up from informal intuitions to a rigorous formal definition, exploring key properties, examples, and the generalization to arbitrary fields. The lecture also introduces the fundamental concept of [linear combinations](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-linear-combination_mc_line-rn-kombinace-linear-combination) of vectors.

### Setting the Stage: Fundamental Mathematical Concepts

Before diving into linear spaces, the lecture briefly touched upon essential mathematical concepts, clarifying what constitutes a definition, a hypothesis, a mathematical theorem (including lemmas and propositions), and a proof. This emphasis underscores the rigorous nature of linear algebra as a branch of mathematics.

### Informal Introduction to Linear Spaces

The lecture began with an intuitive understanding of what a linear space entails. Informally, a linear space over real numbers is any collection of "objects" (which we call [vectors](https://felwiki.basta.one/en/Concepts/vektor_mc_vektor)) that can be added together, and each of which can be multiplied by a [scalar](https://felwiki.basta.one/en/Concepts/skal-r_mc_skal-r) (a real number in this context). These operations, vector addition and scalar multiplication, must adhere to specific rules or "laws."

Several examples were provided to illustrate this informal idea:
*   **Vectors in a plane:** This provides a strong physical and geometric intuition, where operations like vector addition (e.g., $OC = OA + OB$) and scalar multiplication (e.g., $OY = \sqrt{2} OX$, $OZ = -\sqrt{2} OX$) naturally satisfy these rules.
*   **Real polynomials:** Represented as $R[x]$, polynomials can be added and multiplied by real numbers.
*   **n-tuples of real numbers:** Denoted as $R^n$ (for $n > 0$), these are familiar from coordinate geometry.
*   **Complex numbers:** Represented as $C$, complex numbers also form a linear space over $R$.
*   Many other examples exist.

### The Formal Definition of a Linear Space over R

The core of the lecture was the precise definition of a [linear space over R](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-r_mc_line-rn-prostor-nad-r). A [linear space (over R)](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-r_mc_line-rn-prostor-nad-r) is defined as a set $L$ equipped with two operations:
*   Vector addition: $+: L \times L \rightarrow L$
*   Scalar multiplication: $\cdot: R \times L \rightarrow L$

These operations must satisfy eight axioms, which are categorized into properties of vector addition, properties of scalar multiplication, and distributive laws.

**Properties of Vector Addition:**
1.  **Existence of a [Zero Vector](https://felwiki.basta.one/en/Concepts/nulov-vektor-zero-vector_mc_nulov-vektor-zero-vector):** There exists an element $o \in L$ such that for all $x \in L$, $x + o = o + x = x$.
2.  **Associativity of Vector Addition:** For all $x, y, z \in L$, $(x + y) + z = x + (y + z)$.
3.  **Commutativity of Vector Addition:** For all $x, y \in L$, $x + y = y + x$.
4.  **Existence of an [Opposite Vector](https://felwiki.basta.one/en/Concepts/opa-n-vektor-opposite-vector_mc_opa-n-vektor-opposite-vector):** For every $x \in L$, there exists exactly one $y \in L$ (denoted as $-x$) such that $x + y = o$.

**Properties of Scalar Multiplication:**
5.  **Multiplication by Unit Scalar:** For all $x \in L$, $1 \cdot x = x$.
6.  **Associativity of Scalar Multiplication:** For all $a, b \in R$ and all $x \in L$, $a \cdot (b \cdot x) = (a \cdot b) \cdot x$.

**Distributive Laws (connecting both operations):**
7.  **Distributivity of Scalar Sum:** For all $a, b \in R$ and all $x \in L$, $(a + b) \cdot x = a \cdot x + b \cdot x$.
8.  **Distributivity of Vector Sum:** For all $a \in R$ and all $x, y \in L$, $a \cdot (x + y) = a \cdot x + a \cdot y$.

### Simple Consequences and Important Theorems

From these fundamental axioms, several important properties can be derived:
*   The [zero vector](https://felwiki.basta.one/en/Concepts/nulov-vektor-zero-vector_mc_nulov-vektor-zero-vector) is unique.
*   For any vector $x \in L$, $0 \cdot x = o$.
*   The [opposite vector](https://felwiki.basta.one/en/Concepts/opa-n-vektor-opposite-vector_mc_opa-n-vektor-opposite-vector) to $x \in L$ is given by $(-1) \cdot x$. Specifically, $x + (-1) \cdot x = 1 \cdot x + (-1) \cdot x = (1 - 1) \cdot x = 0 \cdot x = o$.
*   For any [scalar](https://felwiki.basta.one/en/Concepts/skal-r_mc_skal-r) $a \in R$, $a \cdot o = o$.

A particularly crucial consequence is the theorem stating:
"Let $L$ be a [linear space](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-r_mc_line-rn-prostor-nad-r), $a \in R$, $x \in L$. Then $a \cdot x = o$ if and only if $a = 0$ or $x = o$."
This theorem is proven by leveraging the existence of multiplicative inverses for non-zero real numbers, which is a key property of the scalar field.

### Further Examples and Counterexamples

The lecture reinforced the understanding of linear spaces with additional examples and counterexamples:
*   **Example (0, +∞) with redefined operations:** The set of positive real numbers $L = (0, +\infty)$ can form a [linear space](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-r_mc_line-rn-prostor-nad-r) with non-standard operations defined as:
    *   Vector addition: $x \oplus y := x \cdot y$
    *   Scalar multiplication: $a \odot x := x^a$
*   **Trivial [linear space](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-r_mc_line-rn-prostor-nad-r):** Any single-element set $L = \{o\}$ (with evident operations) constitutes a trivial linear space.
*   **Counterexample R² with non-standard addition:** The set $R^2$ with operations:
    *   $[a, b] + [c, d] := [a+d, b+c]$
    *   $\alpha \cdot [a, b] := [\alpha a, \alpha b]$
    This does *not* form a [linear space](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-r_mc_line-rn-prostor-nad-r) because the commutative property of vector addition ($x + y = y + x$) would fail.

### Generalization: Linear Spaces over an Arbitrary Field

The lecture also touched upon the role of real numbers as [scalars](https://felwiki.basta.one/en/Concepts/skal-r_mc_skal-r) and introduced the concept of a more general structure: a [linear space over a field F](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-t-lesem-f-linear-space-over-field-f---vector-space-over-field-f). This involves replacing $R$ with an abstract algebraic structure called a [field (těleso)](https://felwiki.basta.one/en/Concepts/t-leso-field_mc_t-leso-field), which essentially means the [scalars](https://felwiki.basta.one/en/Concepts/skal-r_mc_skal-r) must possess well-behaved addition, multiplication, and inverses. This abstraction represents a further generalization beyond just real numbers, allowing for linear algebra to be applied to other number systems (like complex numbers or finite fields).

### Linear Combinations: The Fundamental Operation

A crucial concept introduced was the idea of a [linear combination](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-linear-combination_mc_line-rn-kombinace-linear-combination) of vectors. In a [linear space](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-r_mc_line-rn-prostor-nad-r), the most general computation one can perform is to sum a finite number of scalar multiples of vectors. Given a finite list of [vectors](https://felwiki.basta.one/en/Concepts/vektor_mc_vektor) $(x_1, \dots, x_n)$ and a corresponding list of [scalars](https://felwiki.basta.one/en/Concepts/skal-r_mc_skal-r) $(a_1, \dots, a_n)$ called [coefficients of the linear combination](https://felwiki.basta.one/en/Concepts/koeficienty-line-rn-kombinace-coefficients-of-a-linear-combination_mc_koeficienty-lineární-kombinace-coefficients-of-a-linear-combination), a [linear combination](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-linear-combination_mc_line-rn-kombinace-linear-combination) is expressed as:
$$a_1x_1 + a_2x_2 + \dots + a_nx_n$$
This can also be written using summation notation: $\sum_{i=1}^{n} a_ix_i$ or $\sum_{i \in \{1, \dots, n\}} a_ix_i$.

A key distinction was made between a "list" (or sequence) of [vectors](https://felwiki.basta.one/en/Concepts/vektor_mc_vektor) and a "set" of [vectors](https://felwiki.basta.one/en/Concepts/vektor_mc_vektor). In a list, the order and multiplicity of elements matter (e.g., $(x_1, x_2, x_3) \neq (x_3, x_2, x_1)$ and $(x_1, x_1, x_2) \neq (x_1, x_2)$), which is crucial for defining linear combinations. For an empty list of vectors, the [zero vector](https://felwiki.basta.one/en/Concepts/nulov-vektor-zero-vector_mc_nulov-vektor-zero-vector) $o$ is defined as its (only possible) [linear combination](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-linear-combination_mc_line-rn-kombinace-linear-combination) with an empty list of coefficients.

The lecture concluded with a "slogan" for intuitive understanding: [linear combinations](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-linear-combination_mc_line-rn-kombinace-linear-combination) of a list of [vectors](https://felwiki.basta.one/en/Concepts/vektor_mc_vektor) in $R^n$ create a "flat piece" of $R^n$ that passes through the origin and has the direction of the given vectors. This concept will lead to the definition of linear subspaces in future lectures. The lecturer emphasized that such "slogans" are for intuition only and cannot replace precise mathematical definitions and theorems.

### Keywords
Linear Algebra, Vector Spaces, Mathematical Definitions, [Linear Combinations](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-linear-combination_mc_line-rn-kombinace-linear-combination), [Field Theory](https://felwiki.basta.one/en/Concepts/t-leso-field_mc_t-leso-field)