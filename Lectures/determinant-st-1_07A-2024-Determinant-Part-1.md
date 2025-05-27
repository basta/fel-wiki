# Determinant: část 1
## Lineární algebra - Lecture 1

**Speaker:** Jiří Velebil

This lecture serves as the foundational introduction to the **determinant** of a square matrix, a crucial concept in [Linear Algebra](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-t-lesem-f-linear-space-over-field-f---vector-space-over-field-f.md). Building upon previous discussions of [Gaussian Elimination Method (GEM)](https://felwiki.basta.one/en/Concepts/gaussian-elimination-method-gem_mc_gaussian-elimination-method-gem) and the regularity/singularity of square [matrices](https://felwiki.basta.one/en/Concepts/matice_mc_matice), the determinant is presented not only as a powerful test for matrix invertibility but also, importantly, for its profound geometric significance. The discussion begins by revisiting essential facts about permutations, which are integral to the determinant's definition.

### Permutations and Their Properties

The lecture commenced by defining a [permutation](https://felwiki.basta.one/en/Concepts/permutace_mc_permutace) of a set `{1, 2, ..., n}` as any [bijection](https://felwiki.basta.one/en/Concepts/bijekce_mc_bijekce) from that set to itself. Various notations for permutations were introduced, including explicit mapping (`1↦2, 2↦3, 3↦4, 4↦1`), table representation (`[[1 2 3 4], [2 3 4 1]]`), and the intuitive graphical notation of [string diagrams](https://felwiki.basta.one/en/Concepts/strunov-diagramy_mc_strunové-diagramy). String diagrams are read from top to bottom and are particularly useful for visualizing the composition of permutations.

The collection of all permutations of an n-element set, along with the operation of composition, forms what is known as the [symmetric group of permutations (Sn)](https://felwiki.basta.one/en/Concepts/symetrick-grupa-permutac-sn_mc_symetrická-grupa-permutací-sn). This group possesses key properties: composition is associative, there exists an identity permutation (denoted $id_n$), and every permutation $\pi$ has an inverse $\pi^{-1}$.

A critical concept for defining the determinant is the [sign of a permutation (sign π)](https://felwiki.basta.one/en/Concepts/znam-nko-permutace-sign_mc_znaménko-permutace-sign-π). The sign of a permutation $\pi$ is defined as +1 if its string diagram contains an even number of string crossings (an "even" permutation), and -1 if it contains an odd number of crossings (an "odd" permutation). Important properties of the permutation sign were highlighted:
*   $\text{sign}(id_n) = 1$
*   $\text{sign}(\sigma \cdot \pi) = (\text{sign } \sigma) \cdot (\text{sign } \pi)$ for any permutations $\sigma, \pi \in S_n$.
*   $\text{sign } \pi = \text{sign}(\pi^{-1})$.
*   Swapping two values in a permutation changes its sign: $\text{sign } \sigma = - \text{sign } \pi$ if $\sigma$ is obtained by swapping two values in $\pi$.

### Defining the Determinant

With permutations in hand, the lecture proceeded to define the [determinant of a square matrix (det(A) or |A|)](https://felwiki.basta.one/en/Concepts/determinant-tvercov-matice-det-a-or-a_mc_determinant-čtvercové-matice-deta-or-a). For an $n \times n$ matrix $A$ over a field $F$, the determinant is a scalar value defined by the formula:

$$
\text{det}(A) = \sum_{\pi \in S_n} \text{sign } \pi \cdot a_{\pi(1),1} \cdot a_{\pi(2),2} \cdots a_{\pi(n),n}
$$

This formula sums over all $n!$ permutations in $S_n$. Each term in the sum is a product of $n$ matrix elements, where each element comes from a unique row and a unique column, effectively like placing non-threatening rooks on a chessboard. The sign of the permutation determines whether the term is added or subtracted.

For $3 \times 3$ matrices, this definition simplifies to [Sarrus' rule](https://felwiki.basta.one/en/Concepts/sarrusovo-pravidlo_mc_sarrusovo-pravidlo):

$$
\text{det}(A) = a_{11}a_{22}a_{33} + a_{21}a_{32}a_{13} + a_{31}a_{12}a_{23} - a_{21}a_{12}a_{33} - a_{11}a_{32}a_{23} - a_{31}a_{22}a_{13}
$$

### Geometric Interpretation of the Determinant

Beyond its algebraic definition, the determinant holds a crucial geometric meaning. For a $2 \times 2$ matrix over $\mathbb{R}$, its determinant represents the oriented area of the parallelogram formed by its column vectors. This orientation is significant:
*   The area is positive if the second vector is counter-clockwise from the first.
*   Swapping the order of vectors changes the sign of the area: $P(\mathbf{a}, \mathbf{b}) = -P(\mathbf{b}, \mathbf{a})$.
*   The area function $P(\mathbf{a}, \mathbf{b})$ is linear in each argument, meaning operations like $P(c_1 \mathbf{a}_1 + c_2 \mathbf{a}_2, \mathbf{b}) = c_1 P(\mathbf{a}_1, \mathbf{b}) + c_2 P(\mathbf{a}_2, \mathbf{b})$ hold. A significant consequence is that adding a scalar multiple of one vector to another does not change the area of the parallelogram, e.g., $P(\mathbf{a}, \mathbf{b}) = P(\mathbf{a}, \mathbf{b} - 2\mathbf{a})$.

This geometric interpretation generalizes to higher dimensions: the determinant of an $n \times n$ matrix $A = (\mathbf{a}_1, ..., \mathbf{a}_n)$ represents the oriented volume $V(\mathbf{a}_1, ..., \mathbf{a}_n)$ of the parallelepiped (or *n*-dimensional hyper-parallelepiped) defined by its column vectors. This volume function $V$ is characterized by three properties:
1.  $V(\mathbf{e}_1, ..., \mathbf{e}_n) = 1$ (defining a unit volume).
2.  $V(\mathbf{a}_1, ..., \mathbf{a}_n) = \text{sign } \pi \cdot V(\mathbf{a}_{\pi(1)}, ..., \mathbf{a}_{\pi(n)})$ (swapping vectors changes the sign).
3.  $V(\mathbf{a}_1, ..., \mathbf{a}_n)$ is linear in each coordinate.

These three properties uniquely define the determinant.

### Properties and Calculation Methods

The lecture also covered fundamental properties that greatly simplify the calculation of determinants:
*   **Determinant of a Transpose:** The determinant of a matrix is equal to the determinant of its transpose: $\text{det}(A) = \text{det}(A^T)$. This means any row operation property also applies to column operations.
*   **Effect of Elementary Row Operations:**
    *   Swapping two rows changes the sign of the determinant.
    *   Multiplying a row by a non-zero scalar $\alpha$ multiplies the determinant by $\alpha$.
    *   Adding a scalar multiple of one row to another row does not change the determinant.

These properties are crucial for calculating the [determinant using GEM](https://felwiki.basta.one/en/Concepts/v-po-et-determinantu-pomoc-gem_mc_výpočet-determinantu-pomocí-gem). By reducing a matrix to an upper triangular form (where the determinant is simply the product of its diagonal elements), one can find the determinant of the original matrix by accounting for the changes introduced by row operations. This method is generally more efficient than computing from the definition, scaling roughly as $n^3$ operations, compared to $n!$ for the definition.

### Determinant and Matrix Invertibility

A cornerstone theorem presented states the direct link between the determinant and a matrix's [invertibility](https://felwiki.basta.one/en/Concepts/invertibilita-matice_mc_invertibilita-matice) (or regularity):

For an $n \times n$ matrix $A$ over a field $F$, $A$ is [regular (invertible)](https://felwiki.basta.one/en/Concepts/regul-rn-matice-regular-matrix_mc_regulární-matice-regular-matrix) if and only if $\text{det}(A) \neq 0$. If $\text{det}(A) = 0$, the matrix is [singular](https://felwiki.basta.one/en/Concepts/singul-rn-matice_mc_singulární-matice) and not invertible.

While the definition provides theoretical insight, direct computation from the definition is computationally expensive due to the $n!$ terms. The [Gaussian Elimination Method](https://felwiki.basta.one/en/Concepts/gaussova-elimina-n-metoda-gem_mc_gaussova-eliminační-metoda-gem) offers a more practical approach, though care must be taken with numerical stability over real or complex fields. The next lecture will delve into other methods, such as cofactor expansion (Laplace expansion), which offers a recursive approach.

### Optional Advanced Perspective

The lecture briefly touched upon an alternative, more abstract way to introduce the determinant through exterior algebra (specifically, the exterior power of a linear space). This approach offers an immediate geometric understanding and simplifies proofs of determinant properties. It also extends the concept to general linear transformations, not just matrices, and is foundational for geometric algebra, a tool used in computer graphics.

### Key Takeaways

*   The determinant is a scalar value associated with a square matrix, serving as a test for its invertibility.
*   Understanding [permutations](https://felwiki.basta.one/en/Concepts/permutace_mc_permutace) and their [signs](https://felwiki.basta.one/en/Concepts/znam-nko-permutace-sign_mc_znaménko-permutace-sign-π) is fundamental to the determinant's definition.
*   The [determinant](https://felwiki.basta.one/en/Concepts/determinant-tvercov-matice-det-a-or-a_mc_determinant-čtvercové-matice-deta-or-a) has a clear geometric meaning as the oriented volume of the parallelepiped spanned by the matrix's column vectors.
*   Methods for calculation include [Sarrus' rule](https://felwiki.basta.one/en/Concepts/sarrusovo-pravidlo_mc_sarrusovo-pravidlo) for $3 \times 3$ matrices and the [Gaussian Elimination Method](https://felwiki.basta.one/en/Concepts/gaussova-elimina-n-metoda-gem_mc_gaussova-eliminační-metoda-gem), which requires careful tracking of row operations.
*   A matrix is [invertible (regular)](https://felwiki.basta.one/en/Concepts/invertibilita-matice_mc_invertibilita-matice) if and only if its determinant is non-zero.

---

**Keywords:** Permutations, Determinants, Linear Algebra, Matrix Theory, Gaussian Elimination