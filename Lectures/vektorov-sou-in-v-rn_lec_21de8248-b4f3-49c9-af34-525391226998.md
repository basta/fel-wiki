# Vektorový součin v Rn
## Lineární algebra - 12B-2024
**Speaker:** Jiří Velebil

This lecture provides a comprehensive introduction to the [Gram determinant](https://felwiki.basta.one/en/Concepts/gram-v-determinant_mc_gramův-determinant.md) and the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md) in `R^n`, the n-dimensional Euclidean space. The primary objective is to equip students with the ability to calculate the k-dimensional volume of a parallelepiped and to understand the formal definition and properties of the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md) for `n ≥ 2`. The concepts discussed, particularly the [standardní skalární součin](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in_mc_standardní-skalární-součin.md), will serve as a foundation for determining the distance between [afinní podprostor](https://felwiki.basta.one/en/Concepts/afinn-podprostor_mc_afinní-podprostor.md)s in future lectures.

### Calculating k-Dimensional Volume with the Gram Determinant

The lecture begins by addressing the problem of how to find the non-oriented k-dimensional [objem k-rovnoběžnostěnu](https://felwiki.basta.one/en/Concepts/objem-k-rovnoběžnostěnu_mc_objem-k-rovnoběžnostěnu.md) in `R^n` when given a list of `k` vectors `(a1,..., ak)`, where `k ≤ n`.
If `k = n`, the volume $V_n(a_1,...,a_n)$ is simply the absolute value of the determinant of the matrix `A` formed by these vectors. However, if `k < n`, the matrix `A` is not square, and its determinant is undefined.

To address this, the lecture introduces the [Gramova matice](https://felwiki.basta.one/en/Concepts/gramova-matice_mc_gramova-matice.md) and the [Gramův determinant](https://felwiki.basta.one/en/Concepts/gram-v-determinant_mc_gramův-determinant.md).
For a matrix `A` (with column vectors `a1,...,ak`), the **Gramova matice** is defined as $A^T A$. This matrix is square and of size `k x k`.
The **Gramův determinant** of a list of vectors `(a1, ..., ak)`, denoted as `Gram(a1, ..., ak)`, is the determinant of their [Gramova matice](https://felwiki.basta.one/en/Concepts/gramova-matice_mc_gramova-matice.md), i.e., $\det(A^T A)$. A key observation is that the element in the j-th column and i-th row of $A^T A$ is the [standardní skalární součin](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in_mc_standardní-skalární-součin.md) $(a_i | a_j)$.

A fundamental theorem presented states the significance of the [Gramův determinant](https://felwiki.basta.one/en/Concepts/gram-v-determinant_mc_gramův-determinant.md):
*   `Gram(a1,...,ak)` is always non-negative ($ \ge 0 $).
*   `Gram(a1,...,ak) > 0` if and only if the vectors `a1,...,ak` are [lineárně nezávislé](https://felwiki.basta.one/en/Concepts/line-rn-nez-vislost_mc_lineární-nezávislost.md).
*   Most importantly, the k-dimensional [objem k-rovnoběžnostěnu](https://felwiki.basta.one/en/Concepts/objem-k-rovnoběžnostěnu_mc_objem-k-rovnoběžnostěnu.md) spanned by `(a1,...,ak)` is given by the square root of their [Gramův determinant](https://felwiki.basta.one/en/Concepts/gram-v-determinant_mc_gramův-determinant.md):
    $$V_k(a_1,...,a_k) = \sqrt{\det(A^T A)} = \sqrt{\text{Gram}(a_1,...,a_k)}$$

**Examples:**
*   **In R³:** To find the 2-dimensional volume of the parallelepiped defined by `a1 = (1, 2, 0)^T` and `a2 = (3, 2, 0)^T`:
    The [Gramova matice](https://felwiki.basta.one/en/Concepts/gramova-matice_mc_gramova-matice.md) is $\begin{pmatrix} (a_1|a_1) & (a_1|a_2) \\ (a_2|a_1) & (a_2|a_2) \end{pmatrix} = \begin{pmatrix} 5 & 7 \\ 7 & 13 \end{pmatrix}$.
    The [Gramův determinant](https://felwiki.basta.one/en/Concepts/gram-v-determinant_mc_gramův-determinant.md) is $\det \begin{pmatrix} 5 & 7 \\ 7 & 13 \end{pmatrix} = 5 \times 13 - 7 \times 7 = 65 - 49 = 16$.
    The volume is $\sqrt{16} = 4$.
*   **In R⁴:** To find the 3-dimensional volume of the parallelepiped defined by `a1 = (2, 1, 1, 3)^T`, `a2 = (-1, 1, 1, 0)^T`, and `a3 = (1, 1, 1, 0)^T`:
    The [Gramova matice](https://felwiki.basta.one/en/Concepts/gramova-matice_mc_gramova-matice.md) is $\begin{pmatrix} 15 & 0 & 4 \\ 0 & 3 & 1 \\ 4 & 1 & 3 \end{pmatrix}$.
    The [Gramův determinant](https://felwiki.basta.one/en/Concepts/gram-v-determinant_mc_gramův-determinant.md) is $\det \begin{pmatrix} 15 & 0 & 4 \\ 0 & 3 & 1 \\ 4 & 1 & 3 \end{pmatrix} = 72$.
    The volume is $\sqrt{72} \approx 8.485$.

### Definition and Properties of the Vector Product

The lecture then transitions to the formal definition of the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md) in `R^n` for `n ≥ 2`. It starts by recalling that any linear transformation $f: R^n \to R$ can be uniquely represented as a [standardní skalární součin](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in_mc_standardní-skalární-součin.md) $f(x) = a^T \cdot x = (a | x)$ for some unique vector `a` in `R^n`.

For a given list of `n-1` vectors `(x1,...,xn-1)` in `R^n`, the mapping from `x` to $\det(x_1,...,x_{n-1}, x)$ is linear. This crucial observation leads to the definition of the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md):
The **vektorový součin** of `(x1,...,xn-1)`, denoted `×(x1,...,xn-1)`, is the unique vector `a` in `R^n` such that for all `x` in `R^n`:
$$(\times(x_1,...,x_{n-1}) | x) = \det(x_1,...,x_{n-1}, x)$$

A fundamental property directly derived from this definition is that the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md) is **orthogonal** to all the vectors `xj` from which it is formed. This is because substituting any `xj` for `x` in the definition results in a determinant with two identical columns, which is zero: $(\times(x_1,...,x_{n-1}) | x_j) = \det(x_1,...,x_{n-1}, x_j) = 0$.

The lecture also provides a formula for computing the components of the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md) using the [standardní skalární součin](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in_mc_standardní-skalární-součin.md) with orthonormal basis vectors `ei`:
$$\times(x_1,...,x_{n-1}) = \sum_{i=1}^{n} \det(x_1,...,x_{n-1}, e_i) \cdot e_i$$

### Computational Examples and Mnemonic Device

The lecture illustrates the computation of the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md) in lower dimensions:

*   **In R²:** For a single vector `x = (x1, x2)^T`, the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md) `×(x)` is calculated as `(-x2, x1)^T`. This is a well-known formula for finding a vector perpendicular to a given 2D vector. For example, `×((6), (12)) = (-12, 6)^T`.

*   **In R³:** For two vectors `x1` and `x2`, the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md) (often written as `x1 × x2`) can be computed using the general formula, which expands to a complex expression in terms of components. For instance, for `x1 = (x11, x21, x31)^T` and `x2 = (x12, x22, x32)^T`, the result is `(x21x32 - x31x22, x31x12 - x11x32, x11x22 - x21x12)^T`.

To make the computation more manageable, especially for higher dimensions, a **mnemonic device** is introduced. This involves a formal determinant-like notation:
$$ \times(x_1,...,x_{n-1}) = \begin{vmatrix} x_{11} & x_{12} & \dots & x_{1,n-1} & e_1 \\ x_{21} & x_{22} & \dots & x_{2,n-1} & e_2 \\ \vdots & \vdots & \ddots & \vdots & \vdots \\ x_{n1} & x_{n2} & \dots & x_{n,n-1} & e_n \end{vmatrix} $$
Although not a true determinant in the classical sense due to the mix of scalars and basis vectors, one calculates it as if it were a determinant.
*   **Example in R³:** For `x1 = (3, -1, 2)^T` and `x2 = (1, 0, 4)^T`, applying this rule yields `(-4, -10, 1)^T`.
*   **Example in R⁴:** For `x1 = (1,0,0)^T`, `x2 = (0,1,0)^T`, `x3 = (0,0,1)^T` in `R^4`, the result is `(0, 0, -1, 1)^T`.

### Further Properties of the Vector Product

The lecture concludes by summarizing several important properties of the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md), all of which stem directly from the properties of determinants:
*   The function `(x1,...,xn-1) -> ×(x1,...,xn-1)` is **linear in each argument**.
*   It exhibits **alternating behavior** under permutation: `×(xπ(1),..., xπ(n-1)) = sign(π) · ×(x1,..., xn-1)` for a permutation `π`.
*   A crucial link to [linear independence](https://felwiki.basta.one/en/Concepts/line-rn-nez-vislost_mc_lineární-nezávislost.md) is established: `×(x1,...,xn-1) = 0` if and only if the vectors `x1,...,xn-1` are [lineárně závislé](https://felwiki.basta.one/en/Concepts/line-rn-z-vislost-seznam-vektor_mc_lineární-závislost-seznam-vektorů.md).
*   Finally, the **[norma](https://felwiki.basta.one/en/Concepts/norma_mc_norma.md) of the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md)** is directly related to the k-dimensional volume, providing a strong geometric interpretation:
    $$||\times(x_1,...,x_{n-1})|| = \sqrt{\text{Gram}(x_1,...,x_{n-1})}$$
    This means the [norma](https://felwiki.basta.one/en/Concepts/norma_mc_norma.md) of the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md) is equal to the `(n-1)`-dimensional [objem k-rovnoběžnostěnu](https://felwiki.basta.one/en/Concepts/objem-k-rovnoběžnostěnu_mc_objem-k-rovnoběžnostěnu.md) determined by the vectors `x1,...,xn-1`.

This lecture laid essential groundwork for understanding multidimensional geometry in `R^n`, particularly for calculating volumes and defining the [vektorový součin](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md). These concepts will be vital for future discussions, such as determining the distance between [afinní podprostor](https://felwiki.basta.one/en/Concepts/afinn-podprostor_mc_afinní-podprostor.md)s in `R^n`.

### Keywords
Vector Product, Gram Determinant, Linear Algebra, Euclidean Space, Multidimensional Volume