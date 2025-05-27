# Lineární závislost a nezávislost

## Lineární algebra - Lecture 02B-2024
**Speaker:** Jiří Velebil

This lecture on Linear Algebra, delivered by Jiří Velebil, delves into the fundamental concepts of [Lineární závislost a nezávislost](https://felwiki.basta.one/en/Concepts/line-rn-z-vislost-nez-vislost-linear-dependence-independence_mc_lineární-závislost-nezávislost-linear-dependence-independence.md) of vectors. Building upon previous discussions on linear combinations, spans, and subspaces, the lecture provides a comprehensive understanding of what it means for a set of vectors to be linearly dependent or independent, offering practical tests and illustrative examples.

### Revisiting Linear Combinations and Spans

The lecture began by recalling key concepts from previous sessions, such as the definition of a [Lineární kombinace](https://felwiki.basta.one/en/Concepts/line-rn-kombinace_mc_lineární-kombinace.md) and the [Lineární obal (span)](https://felwiki.basta.one/en/Concepts/line-rn-obal-span_mc_lineární-obal-span.md) of a set of vectors. A [Lineární obal](https://felwiki.basta.one/en/Concepts/line-rn-obal_mc_lineární-obal.md) forms a [Lineární podprostor](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md). An important point highlighted was the scenario where a vector within a set might be "redundant" concerning the formation of linear combinations. For instance, in $R^3$, if two vectors $a_1$ and $a_2$ are collinear, their span, $\text{span}(\{a_1, a_2\})$, is merely a line, equivalent to $\text{span}(\{a_1\})$. In such a case, $a_2$ is "unnecessary" for spanning the space, a precursor to the concept of linear dependence.

### Trivial, Non-trivial, and Zero Linear Combinations

To formally define linear dependence and independence, the lecture first clarified different types of linear combinations:

*   **[Triviální lineární kombinace](https://felwiki.basta.one/en/Concepts/trivi-ln-line-rn-kombinace_mc_triviální-lineární-kombinace.md)**: A linear combination of the form $a_1 \cdot x_1 + \dots + a_n \cdot x_n$ is considered trivial if all coefficients $a_1, \dots, a_n$ are equal to zero. It's important to note that a trivial linear combination always results in the [Nulový vektor](https://felwiki.basta.one/en/Concepts/nulov-vektor-zero-vector_mc_nulový-vektor-zero-vector.md) ($ \vec{0} $), since $0 \cdot \vec{x} = \vec{0}$ for any vector $\vec{x}$. This can be expressed as:
    $$0 \cdot \vec{x}_1 + \dots + 0 \cdot \vec{x}_n = \vec{0}$$

*   **[Netriviální lineární kombinace](https://felwiki.basta.one/en/Concepts/netrivi-ln-line-rn-kombinace_mc_netriviální-lineární-kombinace.md)**: Conversely, a linear combination is non-trivial if at least one of the coefficients $a_1, \dots, a_n$ is not zero. A crucial insight is that a non-trivial linear combination can still equal the zero vector. For example, $\vec{x} - \vec{x} = \vec{0}$.

*   **[Nulová kombinace](https://felwiki.basta.one/en/Concepts/nulov-kombinace_mc_nulová-kombinace.md)**: This term is used for any linear combination that results in the zero vector. While every trivial combination is by definition a zero combination, a zero combination is *not* necessarily trivial, as demonstrated by the $\vec{x} - \vec{x} = \vec{0}$ example. The general form of a linear combination resulting in the zero vector is:
    $$a_1 \cdot \vec{x}_1 + \dots + a_n \cdot \vec{x}_n = \vec{0}$$
    Here, $a_i$ are scalar coefficients and $x_i$ are vectors.

### Defining Linear Independence and Dependence

The core of the lecture focused on formalizing [Lineární závislost a nezávislost](https://felwiki.basta.one/en/Concepts/line-rn-z-vislost-nez-vislost-linear-dependence-independence_mc_lineární-závislost-nezávislost-linear-dependence-independence.md) for both lists and sets of vectors.

**For a List of Vectors:**

A list $S$ of vectors $(x_1, \dots, x_n)$ is defined as [Lineární nezávislost (seznam vektorů)](https://felwiki.basta.one/en/Concepts/line-rn-nez-vislost-seznam-vektor_mc_lineární-nezávislost-seznam-vektorů.md) if it satisfies one of the following conditions:
1.  The list $S$ is empty.
2.  For any linear combination $a_1 \cdot x_1 + \dots + a_n \cdot x_n = \vec{0}$, it must strictly follow that all coefficients $a_1 = a_2 = \dots = a_n = 0$.

A list $S$ is considered [Lineární závislost (seznam vektorů)](https://felwiki.basta.one/en/Concepts/line-rn-z-vislost-seznam-vektor_mc_lineární-závislost-seznam-vektorů.md) if it is not linearly independent. This implies that there exists at least one non-trivial linear combination of its vectors that sums to the zero vector.

**For a Set of Vectors:**

A set $M$ of vectors in a linear space $L$ is defined as [Lineární nezávislost (množina vektorů)](https://felwiki.basta.one/en/Concepts/line-rn-nez-vislost-mno-ina-vektor_mc_lineární-nezávislost-množina-vektorů.md) if:
1.  The set $M$ is empty.
2.  If $M = \{x_1, \dots, x_n\}$ is a non-empty [konečná množina](https://felwiki.basta.one/en/Concepts/kone-n-mno-ina_mc_konečná-množina.md), then for any linear combination $a_1 \cdot x_1 + \dots + a_n \cdot x_n = \vec{0}$, it must imply that $a_1 = a_2 = \dots = a_n = 0$.
3.  If $M$ is an [nekonečná množina](https://felwiki.basta.one/en/Concepts/nekone-n-mno-ina_mc_nekonečná-množina.md), then every finite subset of $M$ must be linearly independent.

A set $M$ is considered [Lineární závislost (množina vektorů)](https://felwiki.basta.one/en/Concepts/line-rn-z-vislost-mno-ina-vektor_mc_lineární-závislost-množina-vektorů.md) if it is not linearly independent. This means that there is at least one non-trivial linear combination of vectors from $M$ that results in the zero vector. Practically, to test the linear independence of a non-empty set $M$, one must verify that if $a_1 \cdot x_1 + \dots + a_n \cdot x_n = \vec{0}$ for distinct $x_i \in M$, then all $a_i$ must be zero.

### Illustrative Examples

The lecture provided several examples to solidify these definitions:

*   The empty list `()` is always linearly independent.
*   A list containing the [Nulový vektor](https://felwiki.basta.one/en/Concepts/nulov-vektor-zero-vector_mc_nulový-vektor-zero-vector.md), like `(o)`, is always linearly dependent, as $1 \cdot \vec{0} = \vec{0}$ is a non-trivial zero combination.
*   Any list or set where a vector is repeated (e.g., $(x, x)$) is linearly dependent, because $1 \cdot x - 1 \cdot x = \vec{0}$ is a non-trivial zero combination.
*   In $R^3$, the set of standard basis vectors $\{[[0],[1],[0]], [[1],[0],[0]], [[0],[0],[1]]\}$ is linearly independent. Generally, for $i=1, \dots, n$, the vectors $e_i \in R^n$ (having 1 at the $i$-th position and 0 elsewhere) form a linearly independent set $\{e_1, \dots, e_n\}$ in $R^n$.
*   An interesting example of an infinite linearly independent set is $\{1, x, x^2, x^3, \dots\}$ in the space of polynomials $R[x]$.
*   Conversely, the set $\{[[1],[-7],[3]], [[-1],[2],[1]], [[1],[8],[-9]]\}$ in $R^3$ is linearly dependent. This was demonstrated by the non-trivial linear combination:
    $$2 \cdot \begin{bmatrix} 1 \\ -7 \\ 3 \end{bmatrix} + 3 \cdot \begin{bmatrix} -1 \\ 2 \\ 1 \end{bmatrix} + 1 \cdot \begin{bmatrix} 1 \\ 8 \\ -9 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix}$$
    This example clearly shows that coefficients ($2, 3, 1$) are not all zero, yet the sum is the zero vector.
*   A key connection was made to systems of linear equations: a set of vectors $(a_1, \dots, a_s)$ is linearly independent if and only if the corresponding homogeneous system of linear equations ($X_1 a_{11} + \dots + X_s a_{1s} = 0$, etc.) has only the trivial solution ($X_1 = \dots = X_s = 0$).

### Properties of Linearly Dependent and Independent Sets

The lecture concluded by presenting important theorems and properties concerning how linear dependence and independence behave when vectors are added or removed from sets:

*   **Subsets of Linearly Independent Sets:** If $M$ is a [Lineární nezávislost (množina vektorů)](https://felwiki.basta.one/en/Concepts/line-rn-nez-vislost-mno-ina-vektor_mc_lineární-nezávislost-množina-vektorů.md) of vectors in a linear space $L$, then any subset $N \subseteq M$ is also linearly independent. The helpful slogan for this is: "If we remove some vectors from a linearly independent set, the resulting set is still linearly independent."

*   **Supersets of Linearly Dependent Sets:** Conversely, if $M$ is a [Lineární závislost (množina vektorů)](https://felwiki.basta.one/en/Concepts/line-rn-z-vislost-mno-ina-vektor_mc_lineární-závislost-množina-vektorů.md) of vectors in $L$, and $N$ is any set of vectors in $L$ such that $M \subseteq N$, then $N$ is also linearly dependent. The corresponding slogan is: "If we add some vectors to a linearly dependent set, the resulting set is still linearly dependent."

*   **Characterization of Linearly Independent Sets:** For a set $M$ of vectors in a linear space $L$, the following conditions are equivalent:
    1.  The set $M$ is linearly independent.
    2.  For every vector $\vec{x} \notin \text{span}(M)$, the set $M \cup \{\vec{x}\}$ is linearly independent. This means that if a vector is not already in the span of an independent set, adding it will maintain independence.

*   **Characterization of Linearly Dependent Sets:** For a set $M$ of vectors in a linear space $L$, the following conditions are equivalent:
    1.  The set $M$ is linearly dependent.
    2.  There exists a vector $\vec{v} \in M$ such that removing $\vec{v}$ does not change the [Lineární obal (span)](https://felwiki.basta.one/en/Concepts/line-rn-obal-span_mc_lineární-obal-span.md) of the set, i.e., $\text{span}(M \setminus \{\vec{v}\}) = \text{span}(M)$. This fundamentally means that at least one vector in a linearly dependent set can be expressed as a linear combination of the others, making it "redundant" for spanning purposes.

These equivalences provide powerful tools for understanding and proving properties related to linear dependence and independence in various contexts of linear algebra.

---
### Keywords
Lineární algebra, Lineární závislost, Lineární nezávislost, Vektory, Matematika