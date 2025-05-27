# Báze a dimense
## Lineární algebra - Lecture 3
Speaker: Jiří Velebil

This lecture, the third in the Lineární algebra course, delved into the fundamental concepts of [Lineární algebra](https://felwiki.basta.one/en/Concepts/line-rn-algebra), specifically focusing on generating sets, bases, and the dimension of vector spaces. The primary aim was to define these crucial terms, illustrate them with examples, and discuss their properties. Intuitively, a basis can be thought of as a selection of coordinate axes, while dimension represents the number of such axes needed to describe the space. For further study, the content covered corresponds to chapters 3.1-3.3 and 3.6 of the textbook "Abstraktní a konkrétní lineární algebra."

### Revisiting Fundamental Concepts

The lecture began by recalling essential concepts from previous sessions, which are prerequisite for understanding today's topics: [Lineární kombinace (Linear Combination)](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-linear-combination), [Lineární závislost/nezávislost (Linear Dependence/Independence)](https://felwiki.basta.one/en/Concepts/line-rn-z-vislost-nez-vislost-linear-dependence-independence), and the [Lineární obal (Linear Span)](https://felwiki.basta.one/en/Concepts/line-rn-obal-linear-span) of a list or set of vectors.

### Generating Sets and Finitely Generated Subspaces

The core discussion initiated with the formal definition of a **generating set**. A set $G$ is said to be a [Množina generátorů (Generating Set)](https://felwiki.basta.one/en/Concepts/mno-ina-gener-tor-generating-set) for a linear subspace $W$ of a space $L$ if its linear span, $span(G)$, equals $W$. This can be expressed as:

$$span(G) = W$$

A linear subspace $W$ is then defined as a [Konečně generovaný podprostor (Finitely Generated Subspace)](https://felwiki.basta.one/en/Concepts/kone-n-generovan-podprostor-finitely-generated-subspace) if there exists a finite set $G$ that generates $W$.

Several examples illustrate these definitions:
*   Any linear space $L$ itself is a generating set for $L$. However, this set is generally infinite and linearly dependent (e.g., $\mathbb{R}^2$ is an infinite, linearly dependent generating set for $\mathbb{R}^2$).
*   For the trivial space $\{0\}$, both the empty set $\emptyset$ and the set $\{0\}$ are finite generating sets, as $span(\emptyset) = \{0\}$ and $span(\{0\}) = \{0\}$. It's noteworthy that $\emptyset$ is linearly independent, while $\{0\}$ is linearly dependent.
*   A finite set like $G = \{(-1), (1)\}$ generates the "first and third quadrant axis" in $\mathbb{R}^2$, yet this set $G$ is linearly dependent.

### The Concept of a Basis

Building upon generating sets, the lecture introduced the fundamental concept of a **basis**. A [Báze (Basis)](https://felwiki.basta.one/en/Concepts/b-ze-basis) of a linear space $L$ is defined as a linearly independent set $B$ that also generates $L$. If $B$ is finite, the ordered list of its elements is called an [Uspořádaná báze (Ordered Basis)](https://felwiki.basta.one/en/Concepts/uspo-dan-b-ze-ordered-basis).

A key example is the [Kanonická báze / Standardní báze (Canonical Basis / Standard Basis)](https://felwiki.basta.one/en/Concepts/kanonick-b-ze---standardn-b-ze-canonical-basis---standard-basis) for $F^n$, where $F$ is any field. For $n \ge 1$, the list $K_n = (e_1, ..., e_n)$, where $e_i$ has a one in the $i$-th position and zeros elsewhere, forms an ordered basis for $F^n$. For instance, in $\mathbb{R}^3$, the canonical basis consists of $e_1=(1,0,0)$, $e_2=(0,1,0)$, and $e_3=(0,0,1)$. Another interesting example is the Fourier basis for $\mathbb{C}^4$, which is used in applications like JPEG compression.

### Dimension of a Linear Space

A crucial theorem states that every [Konečně generovaný podprostor (Finitely Generated Subspace)](https://felwiki.basta.one/en/Concepts/kone-n-generovan-podprostor-finitely-generated-subspace) has a finite basis. Moreover, all possible bases of a given linear space $L$ share the same number of elements. This profound result is often proved using the Exchange Lemma.

This property leads directly to the definition of **dimension**. A linear space $L$ is said to have [Dimense (Dimension)](https://felwiki.basta.one/en/Concepts/dimense-dimension) $n$, denoted as $dim(L) = n$, if there exists a basis $B$ of $L$ that contains $n$ elements, where $n$ is a natural number. Such a space is called a [Prostor konečné dimense (Finite-dimensional Space)](https://felwiki.basta.one/en/Concepts/prostor-kone-n-dimense-finite-dimensional-space). Consequently, all bases of such a space will have exactly $n$ elements.

Important implications regarding dimension include:
*   If $M$ is a linearly independent subset of a space $L$ with $dim(L) = n$ and $M$ has $m$ elements, then $m \le n$.
*   If $m = n$, then $M$ is linearly independent if and only if $span(M) = L$.

These concepts allow for a classification of [Lineární podprostory](https://felwiki.basta.one/en/Concepts/line-rn-podprostor) of $\mathbb{R}^3$ (and more generally $F^n$):
*   The origin $\{0\}$ (dimension 0, generated by the empty set).
*   Lines passing through the origin (dimension 1, generated by one non-zero vector).
*   Planes passing through the origin (dimension 2, generated by two linearly independent vectors).
*   The entire space $\mathbb{R}^3$ (dimension 3, generated by three linearly independent vectors).

### Theorems on Subspace Dimensions

The lecture presented key theorems concerning the dimensions of sums and intersections of subspaces.

**Equality of Subspaces Theorem:**
For two linear subspaces $W_1$ and $W_2$ of a finite-dimensional space $L$, they are equal if and only if their dimensions are equal, and this dimension is also equal to the dimension of their sum (also called join or union of subspaces), denoted $W_1 \lor W_2$:
$$W_1 = W_2 \quad \text{if and only if} \quad dim(W_1) = dim(W_2) = dim(W_1 \lor W_2)$$
The sum (or join) of subspaces $W_1$ and $W_2$ is denoted as $W_1 \lor W_2 = span(W_1 \cup W_2)$, which is the [spojení lineárních podprostorů](https://felwiki.basta.one/en/Concepts/spojen-line-rn-ch-podprostor).

**Consequence for Frobenius Theorem:**
An important consequence, relevant for the Frobenius theorem, is that for a linear subspace $W$ of a finite-dimensional space $L$, a vector $v$ belongs to $W$ if and only if the dimension of $W$ is equal to the dimension of the sum of $W$ and the span of $v$:
$$v \in W \quad \text{is equivalent to} \quad dim(W) = dim(W \lor span(v))$$

**Dimension of Sum and Intersection Theorem:**
This fundamental theorem provides a relationship between the dimensions of the sum and intersection of two subspaces:
For any two linear subspaces $W_1$ and $W_2$ of a finite-dimensional linear space $L$, the following holds:
$$dim(W_1 \lor W_2) + dim(W_1 \cap W_2) = dim(W_1) + dim(W_2)$$
This formula is often referred to as the "[Princip inkluse a exkluse (Principle of Inclusion-Exclusion)](https://felwiki.basta.one/en/Concepts/princip-inkluse-a-exkluse-principle-of-inclusion-exclusion)" for linear spaces, drawing an analogy to the cardinality formula for finite sets: $card(A \cup B) + card(A \cap B) = card(A) + card(B)$.

### Existence of a Basis and the Axiom of Choice

The lecture also briefly touched upon a more advanced topic: the general existence of a basis for *any* linear space, even infinite-dimensional ones. The theorem states that every linear space $L$ has a basis. However, the proof for this theorem is non-trivial and relies on the [Axiom of Choice (AC)](https://felwiki.basta.one/en/Concepts/axiom-of-choice-ac). The Axiom of Choice, a fundamental axiom in set theory, asserts that for any collection of non-empty sets, it is possible to choose exactly one element from each set. This axiom is independent of the other basic axioms of set theory and is often encountered in an equivalent formulation known as Zorn's Lemma in linear algebra contexts.

### The Importance of the Underlying Field

Finally, a critical point was emphasized: the properties of a linear space, particularly its dimension, are intrinsically linked to the underlying [těleso (field)](https://felwiki.basta.one/en/Concepts/t-leso-field) over which it is defined. The same set of vectors can form a linear space with different characteristics depending on the field.

Consider these examples:
*   The set of all complex numbers $\mathbb{C}$ is a 1-dimensional linear space over the field $\mathbb{C}$ itself. Its basis is, for example, $\{1\}$.
*   The set of all complex numbers $\mathbb{C}$ is a 2-dimensional linear space over the field of real numbers $\mathbb{R}$. Its basis is, for example, $\{1, i\}$.
*   The set of all real numbers $\mathbb{R}$ is a 1-dimensional linear space over the field $\mathbb{R}$. Its basis is $\{1\}$.
*   The set of all real numbers $\mathbb{R}$ is an infinite-dimensional linear space over the field of rational numbers $\mathbb{Q}$. (This requires a non-constructive "Hamel basis").

This highlights the crucial takeaway: when discussing linear spaces, it is essential to always explicitly state the field over which the space is defined, as it fundamentally determines its properties.

### Keywords
Linear Algebra, Vector Spaces, Basis, Dimension, Generating Sets