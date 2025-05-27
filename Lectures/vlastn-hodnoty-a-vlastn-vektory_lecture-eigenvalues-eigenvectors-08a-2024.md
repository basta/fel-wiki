# Vlastní hodnoty a vlastní vektory

## Lineární algebra - Lecture 8

Presented by Jiří Velebil.

This lecture provides a comprehensive introduction to the fundamental concepts of [eigenvalues](https://felwiki.basta.one/en/Concepts/vlastn-hodnota-eigenvalue_mc_vlastní-hodnota-eigenvalue.md) and [eigenvectors](https://felwiki.basta.one/en/Concepts/vlastn-vektor-eigenvector_mc_vlastní-vektor-eigenvector.md), crucial tools for understanding and simplifying [linear transformations](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen-linear-mapping-transformation_mc_lineární-zobrazení-linear-mapping-transformation.md) and matrices. The primary goal is to demonstrate how these concepts facilitate the [diagonalization of matrices](https://felwiki.basta.one/en/Concepts/diagonalisace-matic-matrix-diagonalization_mc_diagonalisace-matic-matrix-diagonalization.md), which in turn provides profound insights into dynamic and recurrent processes.

### The Motivation: Simplifying Linear Transformations

The lecture began by revisiting prior topics, including [matrices of linear transformations](https://felwiki.basta.one/en/Concepts/matice-line-rn-ho-zobrazen_mc_matice-lineárního-zobrazení.md) between finite-dimensional spaces and [coordinate transformation matrices](https://felwiki.basta.one/en/Concepts/matice-transformace-sou-adnic-coordinate-transformation-matrix_mc_matice-transformace-souřadnic-coordinate-transformation-matrix.md). The core challenge introduced for today's lecture was to study general linear transformations $f: L \to L$, where $L$ is a finite-dimensional space. The aim is to identify vectors $x$ for which $f(x) = \lambda x$, a property known as [homothety](https://felwiki.basta.one/en/Concepts/homotetie-homothety_mc_homotetie-homothety.md) – the simplest form of linear transformation from $L$ to $L$. This understanding allows for a strategic change of [basis](https://felwiki.basta.one/en/Concepts/b-ze-basis_mc_báze-basis.md) in $L$ such that the transformation $f$ acts as a homothety along each new basis vector.

### Illustrative Example: Equilibrium of Stochastic Processes

A motivating example from [stochastic processes](https://felwiki.basta.one/en/Concepts/linear-algebra-stochastic-processes-intro_mc_linear-algebra-stochastic-processes-intro.md) was presented using a matrix $A = \begin{pmatrix} 0.3 & 0.7 \\ 0.8 & 0.2 \end{pmatrix}$. The task was to find a non-zero vector $q$ satisfying $A \cdot q = q$. This specific problem relates to finding equilibrium states in such processes and is akin to the algorithm behind Google's PageRank.

For the given matrix, it was quickly noted that $q = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$ is a solution because the row sums of matrix $A$ are 1. However, to approach this problem generally for any matrix $A$, a more systematic method is required. This leads to the central equation $A \cdot x = \lambda x$, which can be rewritten as $(A - \lambda E) \cdot x = o$, where $E$ is the identity matrix. For non-trivial solutions (i.e., non-zero eigenvectors), the matrix $(A - \lambda E)$ must be [singular](https://felwiki.basta.one/en/Concepts/singul-rn-matice_mc_singulární-matice.md). This implies that its [determinant](https://felwiki.basta.one/en/Concepts/determinant-det-a_mc_determinant-deta.md) must be zero:

$$ \text{det}(A - \lambda E) = 0 $$

For the example matrix $A$, the characteristic equation is:
$$ \text{det}\begin{pmatrix} 0.3-\lambda & 0.7 \\ 0.8 & 0.2-\lambda \end{pmatrix} = (0.3-\lambda)(0.2-\lambda) - 0.56 = \lambda^2 - 0.5\lambda - 0.5 = (\lambda - 1)(\lambda + 0.5) = 0 $$

This yields two [eigenvalues](https://felwiki.basta.one/en/Concepts/vlastn-hodnota-eigenvalue_mc_vlastní-hodnota-eigenvalue.md): $\lambda_1 = 1$ and $\lambda_2 = -0.5$.
By substituting these values back into $(A - \lambda E) \cdot x = o$ and solving using [Gaussian Elimination Method (GEM)](https://felwiki.basta.one/en/Concepts/gaussian-elimination-method-gem_mc_gaussian-elimination-method-gem.md):
*   For $\lambda_1 = 1$: The solutions form $\text{span}\left(\begin{pmatrix} 1 \\ 1 \end{pmatrix}\right)$.
*   For $\lambda_2 = -0.5$: The solutions form $\text{span}\left(\begin{pmatrix} -7 \\ 8 \end{pmatrix}\right)$.

These solution spaces are the [eigenspaces](https://felwiki.basta.one/en/Concepts/vlastn-podprostor-eigenspace_mc_vlastní-podprostor-eigenspace.md) corresponding to their respective eigenvalues. The ability to find such a [basis](https://felwiki.basta.one/en/Concepts/b-ze-basis_mc_báze-basis.md) of [eigenvectors](https://felwiki.basta.one/en/Concepts/vlastn-vektor-eigenvector_mc_vlastní-vektor-eigenvector.md) allows the matrix $A$ to be transformed into a [diagonal matrix](https://felwiki.basta.one/en/Concepts/diagon-ln-matice_mc_diagonální-matice.md) $D = \begin{pmatrix} 1 & 0 \\ 0 & -0.5 \end{pmatrix}$ in the basis $B = \left(\begin{pmatrix} 1 \\ 1 \end{pmatrix}, \begin{pmatrix} -7 \\ 8 \end{pmatrix}\right)$. This process, known as [matrix diagonalization](https://felwiki.basta.one/en/Concepts/diagonalisace-matic-matrix-diagonalization_mc_diagonalisace-matic-matrix-diagonalization.md), significantly simplifies the analysis of recurrent processes, where $x_{k+1} = Ax_k$. For instance, if $x_0 = a \begin{pmatrix} 1 \\ 1 \end{pmatrix} + b \begin{pmatrix} -7 \\ 8 \end{pmatrix}$, then $x_n$ can be easily expressed in the new basis as $\text{coords}_B(x_n) = \begin{pmatrix} a \\ (-0.5)^n b \end{pmatrix}$. This illustrates how diagonalization provides a complete overview of the long-term behavior of such systems.

### Key Definitions

The lecture then formally defined the core concepts:

*   **[Eigenvalue](https://felwiki.basta.one/en/Concepts/vlastn-hodnota-eigenvalue_mc_vlastní-hodnota-eigenvalue.md) ($\lambda$):** For a [linear transformation](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen-linear-mapping-transformation_mc_lineární-zobrazení-linear-mapping-transformation.md) $f: L \to L$, a scalar $\lambda$ (from the field F) is an eigenvalue if there exists a non-zero vector $x$ satisfying $f(x) = \lambda x$.
*   **[Eigenvector](https://felwiki.basta.one/en/Concepts/vlastn-vektor-eigenvector_mc_vlastní-vektor-eigenvector.md):** Any such non-zero vector $x$ is called an eigenvector corresponding to the eigenvalue $\lambda$.
*   **[Eigenspace](https://felwiki.basta.one/en/Concepts/vlastn-podprostor-eigenspace_mc_vlastní-podprostor-eigenspace.md):** For any $\lambda$ in $F$, the set of all vectors $x$ satisfying $f(x) = \lambda x$ forms a subspace, denoted $\text{eigen}(\lambda, f)$. This subspace is equivalent to $\text{ker}(f - \lambda \text{id})$. An eigenvalue exists if and only if its eigenspace is non-trivial.

### Matrix Similarity and Characteristic Polynomial

The lecture also revisited the concept of [matrix similarity](https://felwiki.basta.one/en/Concepts/podobnost-matic-matrix-similarity_mc_podobnost-matic-matrix-similarity.md): two matrices $A$ and $B$ are similar ($A \approx B$) if $B = T^{-1}AT$ for some [regular (invertible) matrix](https://felwiki.basta.one/en/Concepts/regul-rn-matice-regular-matrix_mc_regulární-matice-regular-matrix.md) $T$. Similar matrices represent the same linear transformation but with respect to different bases. A crucial property is that similar matrices share the same [characteristic polynomial](https://felwiki.basta.one/en/Concepts/charakteristick-polynom-characteristic-polynomial_mc_charakteristický-polynom-characteristic-polynomial.md).

The [characteristic polynomial](https://felwiki.basta.one/en/Concepts/charakteristick-polynom-characteristic-polynomial_mc_charakteristický-polynom-characteristic-polynomial.md) of an $n \times n$ matrix $A$ is defined as $\text{char}_A(x) = \text{det}(A - xE_n)$, where $E_n$ is the $n \times n$ identity matrix. This polynomial is of degree $n$, and its roots are precisely the eigenvalues of $A$. The theorem states that $\lambda$ is an eigenvalue of $f$ if and only if $\text{det}(A_f - \lambda E_n) = 0$, where $A_f$ is the matrix representation of $f$ in any basis. This result is independent of the chosen basis.

### Diagonalizability and its Conditions

A core problem in linear algebra is determining if a matrix $A$ is [diagonalizable](https://felwiki.basta.one/en/Concepts/diagonalisovateln-matice_mc_diagonalisovatelná-matice.md), meaning if it is similar to a [diagonal matrix](https://felwiki.basta.one/en/Concepts/diagon-ln-matice_mc_diagonální-matice.md) $D$. The condition for this is that $T^{-1}AT = D$ holds for some regular matrix $T$ and diagonal matrix $D = \text{diag}(\lambda_1, \dots, \lambda_n)$. This implies that the columns of $T$ must be [linearly independent](https://felwiki.basta.one/en/Concepts/line-rn-nez-vislost_mc_lineární-nezávislost.md) [eigenvectors](https://felwiki.basta.one/en/Concepts/vlastn-vektor-eigenvector_mc_vlastní-vektor-eigenvector.md) $t_j$, where each $t_j$ corresponds to the eigenvalue $\lambda_j$ from the diagonal of $D$.

A critical theorem states that a matrix $A$ of type $n \times n$ over $F$ is [diagonalizable](https://felwiki.basta.one/en/Concepts/diagonalisovatelnost-matic_mc_diagonalisovatelnost-matic.md) if and only if two conditions are met:
1.  Its [characteristic polynomial](https://felwiki.basta.one/en/Concepts/charakteristick-polynom-characteristic-polynomial_mc_charakteristický-polynom-characteristic-polynomial.md) $\text{char}_A(x)$ can be factored into linear factors over $F$.
2.  For every eigenvalue $\lambda$, its [algebraic multiplicity](https://felwiki.basta.one/en/Concepts/algebraick-n-sobnost-algebraic-multiplicity_mc_algebraická-násobnost-algebraic-multiplicity.md) (its multiplicity as a root of $\text{char}_A(x)$) equals its [geometric multiplicity](https://felwiki.basta.one/en/Concepts/geometrick-n-sobnost-geometric-multiplicity_mc_geometrická-násobnost-geometric-multiplicity.md) (the dimension of its [eigenspace](https://felwiki.basta.one/en/Concepts/vlastn-podprostor-eigenspace_mc_vlastní-podprostor-eigenspace.md) $\text{dim}(\text{eigen}(\lambda, A))$).

The lecture provided an example with two matrices, $A = \begin{pmatrix} 5 & -2 & 2 \\ -1 & 4 & -1 \\ -4 & 4 & -1 \end{pmatrix}$ and $B = \begin{pmatrix} 2 & 4 & -3 \\ -1 & 10 & -6 \\ -1 & 8 & -4 \end{pmatrix}$. Both matrices have the same [characteristic polynomial](https://felwiki.basta.one/en/Concepts/charakteristick-polynom-characteristic-polynomial_mc_charakteristický-polynom-characteristic-polynomial.md), $\text{char}_A(x) = \text{char}_B(x) = -(x-3)^2(x-2)$.
*   For matrix $A$: $\text{dim}(\text{eigen}(3,A)) = 2$ and $\text{dim}(\text{eigen}(2,A)) = 1$. Since these match the algebraic multiplicities, $A$ is [diagonalizable](https://felwiki.basta.one/en/Concepts/diagonalisovateln-matice_mc_diagonalisovatelná-matice.md).
*   For matrix $B$: $\text{dim}(\text{eigen}(3,B)) = 1$ and $\text{dim}(\text{eigen}(2,B)) = 1$. Here, the geometric multiplicity of $\lambda=3$ (which is 1) does *not* equal its algebraic multiplicity (which is 2). Therefore, $B$ is *not* [diagonalizable](https://felwiki.basta.one/en/Concepts/diagonalisovatelnost-matic_mc_diagonalisovatelnost-matic.md), despite having the same characteristic polynomial as $A$. This highlights that identical characteristic polynomials do not guarantee [matrix similarity](https://felwiki.basta.one/en/Concepts/podobnost-matic-matrix-similarity_mc_podobnost-matic-matrix-similarity.md).

### Conclusion and Applications

In summary, the lecture emphasized that finding a basis in which a matrix is [diagonal](https://felwiki.basta.one/en/Concepts/diagon-ln-matice_mc_diagonální-matice.md) (i.e., [diagonalizing the matrix](https://felwiki.basta.one/en/Concepts/diagonalisace-matic-matrix-diagonalization_mc_diagonalisace-matic-matrix-diagonalization.md)) provides a complete understanding of matrix powers ($A^k$) and simplifies the study of complex linear systems. This has wide-ranging applications in fields such as:
*   Theory of dynamic systems.
*   Economics (e.g., Leontief input-output model).
*   Complexity of recursive algorithms (solving [linear homogeneous recurrent equations](https://felwiki.basta.one/en/Concepts/line-rn-homogenn-rekurentn-rovnice_mc_lineární-homogenní-rekurentní-rovnice.md)).
*   Geometry of quadratic forms.
*   Functions of matrices.

The central takeaway is that [eigenvalues](https://felwiki.basta.one/en/Concepts/vlastn-hodnota-eigenvalue_mc_vlastní-hodnota-eigenvalue.md) and [eigenvectors](https://felwiki.basta.one/en/Concepts/vlastn-vektor-eigenvector_mc_vlastní-vektor-eigenvector.md) fundamentally simplify [linear transformations](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen-linear-mapping-transformation_mc_lineární-zobrazení-linear-mapping-transformation.md) to mere scaling operations in a specialized [basis](https://felwiki.basta.one/en/Concepts/b-ze-basis_mc_báze-basis.md), allowing for powerful insights into system behavior, provided the matrix is [diagonalizable](https://felwiki.basta.one/en/Concepts/diagonalisovatelnost-matic_mc_diagonalisovatelnost-matic.md).

### Keywords
Linear Algebra, Eigenvalues, Eigenvectors, Matrix Diagonalization, Stochastic Processes