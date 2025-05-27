# Lineární zobrazení, část 2
## Lineární algebra - Lecture 2
**Speaker:** Jiří Velebil

This lecture, "Linear Transformations, Part 2," continued the exploration of [lineární zobrazení](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen) by delving into their special properties and general matrix representations. Building upon the previous lecture's identification of matrices with specific linear transformations (e.g., A : F^S → F^r mapping `e_j` to the j-th column of A), this session introduced crucial concepts like the kernel, image, defect, and rank, which enable a more refined classification of linear transformations. A significant focus was also placed on understanding the matrix of a general linear transformation `f : L1 → L2` with respect to arbitrary ordered bases, assuming finite dimensions for `L1` and `L2`.

### Special Properties of Linear Transformations

The lecture began by defining special types of [lineární zobrazení](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen):
*   A **[monomorfismus](https://felwiki.basta.one/en/Concepts/monomorfismus)** is an injective (one-to-one) linear transformation.
*   An **[epimorfismus](https://felwiki.basta.one/en/Concepts/epimorfismus)** is a surjective (onto) linear transformation.
*   An **[isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus)** is a bijective (both injective and surjective) linear transformation. Equivalently, an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus) `f` has an inverse transformation `f⁻¹` that is also linear.

A key property discussed is that the composition of monomorphisms, epimorphisms, or isomorphisms results in a monomorphism, epimorphism, or isomorphism, respectively. The identity mapping serves as a fundamental example of an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus).

### Kernel, Image, Defect, and Rank

For a [lineární zobrazení](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen) `f : L1 → L2`, two fundamental concepts are defined:
*   The **[jádro (ker(f))](https://felwiki.basta.one/en/Concepts/j-dro-ker-f)** of `f` is the set of all vectors `x` in `L1` that are mapped to the zero vector in `L2`. Formally, `ker(f) = {x ∈ L1 | f(x) = 0}`.
*   The **[obraz (im(f))](https://felwiki.basta.one/en/Concepts/obraz-im-f)** of `f` is the set of all vectors `f(x)` in `L2` for some `x` in `L1`. Formally, `im(f) = {f(x) | x ∈ L1}`.

It's an important assertion that both the [jádro (ker(f))](https://felwiki.basta.one/en/Concepts/j-dro-ker-f) and the [obraz (im(f))](https://felwiki.basta.one/en/Concepts/obraz-im-f) are subspaces of `L1` and `L2` respectively. Furthermore, for any subspace `W` of `L1`, its image `f(W)` is a subspace of `L2`.

When `L1` is a finite-dimensional space, we can quantify these concepts:
*   The **[defekt (def(f))](https://felwiki.basta.one/en/Concepts/defekt-deff)** of `f` is the dimension of its kernel: `def(f) = dim(ker(f))`.
*   The **[hodnost (rank(f))](https://felwiki.basta.one/en/Concepts/hodnost-rankf)** of `f` is the dimension of its image: `rank(f) = dim(im(f))`.

These two quantities are related by the fundamental **Rank-Nullity Theorem (Věta o dimenzi jádra a obrazu)**:
$$
\text{def}(f) + \text{rank}(f) = \text{dim}(L_1)
$$
This theorem states that the dimension of the domain (`L1`) is equal to the sum of the dimension of the kernel (defect) and the dimension of the image (rank).

### Characterizations of Special Linear Transformations

The concepts of defect and rank allow for concise characterizations of monomorphisms and isomorphisms:

**Characterizations of Monomorphisms:**
For a [lineární zobrazení](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen) `f : L1 → L2` with `L1` being finite-dimensional, the following are equivalent:
*   `f` is a [monomorfismus](https://felwiki.basta.one/en/Concepts/monomorfismus).
*   `def(f) = 0` (i.e., its kernel contains only the zero vector).
*   `f` preserves [lineární nezávislost](https://felwiki.basta.one/en/Concepts/line-rn-nez-vislost) (the image of a linearly independent set is again linearly independent).

A direct consequence is that a matrix `A: F^S → F^r` is a [monomorfismus](https://felwiki.basta.one/en/Concepts/monomorfismus) if and only if the system of equations `A⋅x = o` has only the trivial solution.

**Characterizations of Isomorphisms:**
For a [lineární zobrazení](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen) `f : L1 → L2` with `L1` being finite-dimensional, the following are equivalent:
*   `f` is an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus).
*   `f` is both a [monomorfismus](https://felwiki.basta.one/en/Concepts/monomorfismus) and an [epimorfismus](https://felwiki.basta.one/en/Concepts/epimorfismus).
*   `def(f) = 0` and `im(f) = L2`.
*   `def(f) = 0` and `dim(L1) = dim(L2)`.
*   `f` preserves [lineární nezávislost](https://felwiki.basta.one/en/Concepts/line-rn-nez-vislost), and every equation `f(x) = b` has at least one solution.

This leads to the understanding that a matrix `A: F^S → F^r` is an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus) if and only if `s = r` (the matrix is square) and every system `A⋅x = b` has exactly one solution.

### Regular and Singular Matrices

A square matrix `A : F^n → F^n` is defined as a **[regulární matice](https://felwiki.basta.one/en/Concepts/regul-rn-matice)** (also called invertible or an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus)) if there exists a unique inverse matrix `A⁻¹` such that `A⁻¹ ⋅ A = E_n = A ⋅ A⁻¹`, where `E_n` is the identity matrix. If a matrix is not regular, it is called a **[singulární matice](https://felwiki.basta.one/en/Concepts/singul-rn-matice)**.

An illustrative example is the rotation matrix in `R²` by an angle `α`:
$$
R_{\alpha} = \begin{pmatrix} \cos \alpha & -\sin \alpha \\ \sin \alpha & \cos \alpha \end{pmatrix}
$$
This matrix is [regulární matice](https://felwiki.basta.one/en/Concepts/regul-rn-matice), and its inverse transformation is a rotation by `-α`.

An important consequence for finite-dimensional spaces is that if `dim(L1) = dim(L2) = n`, then for a [lineární zobrazení](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen) `f: L1 → L2`, being a [monomorfismus](https://felwiki.basta.one/en/Concepts/monomorfismus), an [epimorfismus](https://felwiki.basta.one/en/Concepts/epimorfismus), or an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus) are all equivalent conditions.

A powerful example of an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus) is the **Lagrange Interpolation**. Given `n` distinct real numbers `a₁, ..., a_n`, the linear mapping `ev(a₁,...,a_n) : R_{≤n-1}[x] → R^n` defined by `p(x) → (p(a₁), p(a₂), ..., p(a_n))` is a [monomorfismus](https://felwiki.basta.one/en/Concepts/monomorfismus) and thus an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus). This implies that for any `n`-tuple `(b₁, ..., b_n)` in `R^n`, there exists a unique polynomial `P(x)` of degree at most `n-1` such that `P(a_i) = b_i` for all `i`. This unique polynomial is known as the **[Lagrangeův interpolační polynom](https://felwiki.basta.one/en/Concepts/lagrange-v-interpola-n-polynom)**.

Crucially, the lecture highlighted that coordinate calculation itself is an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus). For any ordered [báze](https://felwiki.basta.one/en/Concepts/b-ze-basis) `B = (b₁, ..., b_n)` of a space `L`, the mapping `coordB: L → F^n`, which takes a vector `x` to its coordinate vector `coordB(x)` with respect to `B`, is an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus). This means that from an abstract perspective, all finite-dimensional linear spaces over a field `F` are essentially equivalent to `F^n` for some `n`.

### Matrix Representation of General Linear Transformations

A cornerstone of this lecture was the definition of the **[matice lineárního zobrazení](https://felwiki.basta.one/en/Concepts/matice-line-rn-ho-zobrazen)** with respect to arbitrary ordered bases. Given a [lineární zobrazení](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen) `f : L1 → L2` and ordered bases `B = (b₁, ..., b_s)` for `L1` and `C = (c₁, ..., c_r)` for `L2`, the matrix `A_f` is defined such that:
`coord_C(f(x)) = A_f ⋅ coord_B(x)` for every vector `x` in `L1`.
This means that applying the linear transformation `f` in the abstract spaces `L1` and `L2` is equivalent to multiplying the coordinate vector of `x` (in basis `B`) by `A_f` to obtain the coordinate vector of `f(x)` (in basis `C`). The matrix `A_f` has `r` rows and `s` columns.
The j-th column of `A_f` is formed by the coordinates of `f(b_j)` in basis `C`, i.e., `coord_C(f(b_j))`.

### Composition and Inversion of Linear Transformations via Matrices

The lecture emphasized how matrix multiplication corresponds to the composition of linear transformations. If `f : L1 → L2` has matrix `A_f` (w.r.t. bases `B` and `C`) and `g : L2 → L3` has matrix `A_g` (w.r.t. bases `C` and `D`), then the composite transformation `g⋅f : L1 → L3` has the matrix `A_g ⋅ A_f` (w.r.t. bases `B` and `D`).

Furthermore, for an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus) `f : L1 → L2` (where `dim(L1) = dim(L2) = n`) with matrix `A_f` (w.r.t. bases `B` and `C`), its inverse transformation `f⁻¹` has the matrix `A_f⁻¹` (w.r.t. bases `C` and `B`). This directly links the concept of a [regulární matice](https://felwiki.basta.one/en/Concepts/regul-rn-matice) to being the matrix representation of an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus).

### Practical Examples of Matrix Calculation

The lecture provided examples of calculating matrices for linear transformations:
*   **Differentiation Operator:** For the space of polynomials of degree at most 3, `F_{≤3}[x]`, with basis `B = (x³, x², x¹, 1)`, the differentiation operator `der : F_{≤3}[x] → F_{≤3}[x]` (mapping `a₃x³ + a₂x² + a₁x + a₀` to `3a₃x² + 2a₂x + a₁`) has the following matrix `A_der` with respect to `B`:
    $$
    A_{der} = \begin{pmatrix} 0 & 0 & 0 & 0 \\ 3 & 0 & 0 & 0 \\ 0 & 2 & 0 & 0 \\ 0 & 0 & 1 & 0 \end{pmatrix}
    $$
    Higher order derivatives can then be found by multiplying this matrix by itself.
*   **Change of Basis:** A more complex example involved finding the matrix of a linear transformation `f : R² → R²` with respect to the [kanonická báze](https://felwiki.basta.one/en/Concepts/kanonick-b-ze-canonical-basis) `K₂`, given its behavior with respect to a non-canonical basis `B = ((1,-1), (1,1))`. In basis `B`, `f` is simply a scaling: `f((1,-1)) = 2⋅(1,-1)` and `f((1,1)) = 1/3⋅(1,1)`, so its matrix `A_f` w.r.t. `B` is `((2,0), (0,1/3))`.
    To find the matrix `B_f` w.r.t. `K₂`, the relationship `B_f = S ⋅ A_f ⋅ T` was used, where `S` and `T` are [matice transformace souřadnic](https://felwiki.basta.one/en/Concepts/matice-transformace-sou-adnic) (change-of-basis matrices) relating `B` and `K₂`. Specifically, `S` transforms coordinates from `B` to `K₂`, and `T = S⁻¹` transforms coordinates from `K₂` to `B`.
    For this example, `S = ((1,1),(-1,1))` and `T = ((1/2,1/2),(-1/2,1/2))`.
    The resulting matrix `B_f` in the [kanonická báze](https://felwiki.basta.one/en/Concepts/kanonick-b-ze-canonical-basis) was calculated as:
    $$
    B_f = \begin{pmatrix} 1 & 1 \\ -1 & 1 \end{pmatrix} \cdot \begin{pmatrix} 2 & 0 \\ 0 & 1/3 \end{pmatrix} \cdot \begin{pmatrix} 1/2 & 1/2 \\ -1/2 & 1/2 \end{pmatrix} = \begin{pmatrix} 7/6 & 5/6 \\ -5/6 & 7/6 \end{pmatrix}
    $$
    The lecture concluded by previewing the next topic, which will delve deeper into the conceptual understanding of these [matice transformace souřadnic](https://felwiki.basta.one/en/Concepts/matice-transformace-sou-adnic).

### Keywords
LinearTransformations, Isomorphism, MatrixRepresentation, KernelImage, LinearAlgebra