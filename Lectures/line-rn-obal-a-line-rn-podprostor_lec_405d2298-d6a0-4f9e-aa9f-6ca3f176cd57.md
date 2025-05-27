# Lineární obal a lineární podprostor

## Lineární algebra - Lecture 2

This lecture was delivered by Jiří Velebil.

This lecture, the second in the "Linear Algebra" course, delved into two fundamental concepts: the [linear span](https://felwiki.basta.one/en/Concepts/line-rn-obal_mc_lineární-obal.md) and the [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md). Building upon the previous session's introduction to linear spaces and [linear combinations](https://felwiki.basta.one/en/Concepts/line-rn-kombinace_mc_lineární-kombinace.md), the lecture aimed to provide a comprehensive understanding of how these concepts define the geometric structure within linear spaces. The overall goal was to explain the properties of the [linear span](https://felwiki.basta.one/en/Concepts/line-rn-obal-span_mc_lineární-obal-span.md) and formally define a [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md), illustrating these definitions with various practical examples.

### Review and Basic Concepts

The lecture began with a quick recap of essential notations and concepts from the previous session. It clarified that `-x` is shorthand for `(-1)x`, representing the [opposite vector](https://felwiki.basta.one/en/Concepts/opa-n-vektor_mc_opačný-vektor.md) to `x`, a property derived from the associativity of vector addition. A key reminder was the definition of a [linear combination](https://felwiki.basta.one/en/Concepts/line-rn-kombinace_mc_lineární-kombinace.md) of a list of vectors `(x1, ..., xn)` with coefficients `a1, ..., an` from a field `F` as the vector $\sum_{i=1}^{n} a_i x_i$. Importantly, the [linear combination of an empty list](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-pr-zdn-ho-seznamu_mc_lineární-kombinace-prázdného-seznamu.md) `()` is defined as the zero vector.

Before diving into the main topics, the lecture also provided a brief clarification on the definitions of [finite and infinite sets](https://felwiki.basta.one/en/Concepts/kone-n-mno-ina_mc_konečná-množina.md). A set `M` is considered [finite](https://felwiki.basta.one/en/Concepts/kone-n-mno-ina_mc_konečná-množina.md) if it contains exactly `n` elements for some natural number `n`, where crucially for this lecture, zero is considered a natural number. Conversely, a set `M` is [infinite](https://felwiki.basta.one/en/Concepts/nekone-n-mno-ina_mc_nekonečná-množina.md) if it is not finite, with examples including the sets of natural numbers (N), rational numbers (Q), real numbers (R), complex numbers (C), and polynomial rings (R[x]).

### The [Linear Span](https://felwiki.basta.one/en/Concepts/line-rn-obal_mc_lineární-obal.md)

A central concept introduced was the [linear span](https://felwiki.basta.one/en/Concepts/line-rn-obal-span_mc_lineární-obal-span.md) of a set of vectors. For any set `M` of vectors in a linear space `L`, its [linear span](https://felwiki.basta.one/en/Concepts/line-rn-obal_mc_lineární-obal.md), denoted as `span(M)`, is defined as the set of all possible [linear combinations](https://felwiki.basta.one/en/Concepts/line-rn-kombinace_mc_lineární-kombinace.md) that can be formed from vectors in `M`. That is, a vector `x` belongs to `span(M)` if and only if `x = Σn i=1 ai · xi` for some `n ≥ 0`, coefficients `a1, ..., an` from the field `F`, and vectors `x1, ..., xn` from `M`. It was emphasized that this includes the case of `n=0`, where the [linear combination of an empty set](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-pr-zdn-ho-seznamu_mc_lineární-kombinace-prázdného-seznamu.md) yields the zero vector.

Illustrative examples in `R³` were provided:
*   The [linear span](https://felwiki.basta.one/en/Concepts/line-rn-obal_mc_lineární-obal.md) of a single non-zero vector `{a1}` in `R²` forms a line passing through the origin with direction `a1`.
*   The [linear span](https://felwiki.basta.one/en/Concepts/line-rn-obal_mc_lineární-obal.md) of two linearly independent vectors `{a1, a2}` in `R³` forms a plane passing through the origin with directions `a1` and `a2`.
*   However, a crucial point was raised: if `a2` is a scalar multiple of `a1` (i.e., `a2` "follows" `a1`), then `span({a1, a2})` in `R³` is not a plane but reverts to a line. The lecture noted that the method for distinguishing these cases, which involves the concept of [linear independence](https://felwiki.basta.one/en/Concepts/line-rn-z-vislost-nez-vislost-linear-dependence-independence_mc_lineární-závislost-nezávislost-linear-dependence-independence.md), would be covered in the next lecture.

The lecture then described the "closure properties" of the [linear span](https://felwiki.basta.one/en/Concepts/line-rn-obal_mc_lineární-obal.md):
*   If `M` is a subset of `N`, then `span(M)` is a subset of `span(N)`.
*   Any set `M` is always a subset of its own [linear span](https://felwiki.basta.one/en/Concepts/line-rn-obal_mc_lineární-obal.md) (`M ⊆ span(M)`).
*   Applying the [linear span](https://felwiki.basta.one/en/Concepts/line-rn-obal_mc_lineární-obal.md) operation twice yields the same result: `span(span(M)) ⊆ span(M)`.
These properties imply a key slogan: `span(M)` is the "smallest flat piece" of the linear space that contains `M`, formed by all possible [linear combinations](https://felwiki.basta.one/en/Concepts/line-rn-kombinace_mc_lineární-kombinace.md).

### Defining a [Linear Subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md)

Following the definition of [linear span](https://felwiki.basta.one/en/Concepts/line-rn-obal_mc_lineární-obal.md), the lecture formally defined a [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md). A subset `W` of a linear space `L` is a [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) of `L` if `span(W) ⊆ W`. This can be intuitively understood with the slogan: a [subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) is a "good subset" of the space from which one "cannot escape" by forming any [linear combination](https://felwiki.basta.one/en/Concepts/line-rn-kombinace_mc_lineární-kombinace.md). It was also stated that `span(M)` is always a [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) and represents the smallest [subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) containing `M`.

An equivalent and often more practical set of conditions for a subset `W ⊆ L` to be a [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) was presented:
1.  The zero vector `ō` must be an element of `W` (closure under the zero vector).
2.  For any `x, y ∈ W`, their sum `x + y` must also be in `W` (closure under vector addition).
3.  For any scalar `a` from the field `F` and any vector `x ∈ W`, their scalar product `ax` must also be in `W` (closure under scalar multiplication).
This provides another slogan for a [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md): it always contains the zero vector and "endures" the operations of vector addition and scalar multiplication.

It's important to note the distinction: while any [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) `W` of a linear space `L` is itself a linear space (using the same operations as in `L`), the converse is not generally true. A set can form a linear space on its own, but not be a [subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) of another space. An example was provided for `W = {(x) | x ∈ R}` (which can be considered as `R`) and `R²`. Though `W` is a linear space, it is not a [subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) of `R²`.

Examples illustrating [linear subspaces](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) included:
*   Any linear space is a [subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) of itself.
*   The set containing only the zero vector, `{ō}`, is always a [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) (the "trivial subspace").
*   In `R³`, `W₁ = { (x y z) ∈ R³ | z = 0}` (the xy-plane) is a [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md), while `W₂ = { (x y z) ∈ R³ | z = 1}` (a plane shifted from the origin) is not.
*   The set of real polynomials of degree at most `n`, `R≤n[x]`, is a [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) of `R≤m[x]` if `n ≤ m`. More generally, `F≤n[x]` is a [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) of `F[x]` for any `n ≥ 0`.

### Operations and Properties of [Linear Subspaces](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md)

The lecture also discussed how [linear subspaces](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) behave under set operations:
*   The intersection of any system of subspaces `{Wᵢ | i ∈ I}` of a linear space `L` is always a [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) of `L`.
*   Conversely, the union of a system of [linear subspaces](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) is generally *not* a [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md). This is an important distinction to remember.

To address the union, the concept of the [sum of linear subspaces](https://felwiki.basta.one/en/Concepts/spojen-line-rn-ch-podprostor_mc_spojení-lineárních-podprostorů.md) (called "spojení" in Czech) was introduced. For a system of [linear subspaces](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) `{Wᵢ | i ∈ I}` of `L`, their sum is defined as the [linear subspace](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) formed by `span(∪ᵢ∈I Wᵢ)`. For two subspaces, `W₁` and `W₂`, this is often denoted as `W₁ ∨ W₂`.

### Classification of [Linear Subspaces](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) in `R³`

The lecture concluded by classifying all possible [linear subspaces](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) in `R³`:
1.  The single-element set containing only the origin `{ō}`.
2.  Any line passing through the origin.
3.  Any plane passing through the origin.
4.  The entire `R³` space itself.

While the lecture demonstrated that these are indeed [linear subspaces](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md), the proof that no other types of [subspaces](https://felwiki.basta.one/en/Concepts/line-rn-podprostor_mc_lineární-podprostor.md) exist in `R³` was deferred to a later lecture, as it requires the concept of [dimension](https://felwiki.basta.one/en/Concepts/dimense-dimension_mc_dimense-dimension.md).

**Keywords:** Linear Algebra, Linear Span, Linear Subspace, Vector Spaces, Mathematical Definitions