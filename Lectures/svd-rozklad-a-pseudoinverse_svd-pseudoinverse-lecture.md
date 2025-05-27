# SVD rozklad a pseudoinverse
## Lineární algebra - 11B-2024
Speaker: Jiří Velebil

This lecture provides a comprehensive overview of the [Singular Value Decomposition (SVD)](https://felwiki.basta.one/en/Concepts/singular-value-decomposition-svd_mc_singular-value-decomposition-svd) and its crucial application in defining and computing the [Pseudoinverse (Moore-Penrose inverse)](https://felwiki.basta.one/en/Concepts/pseudoinverse-moore-penrose-inverse_mc_pseudoinverse-moore-penrose-inverse) of a matrix. The session explores the theoretical underpinnings of SVD, its geometric interpretation, and practical applications in fields such as data compression and solving systems of linear equations where traditional inverses do not exist.

### Introduction to Singular Value Decomposition (SVD)

The lecture began by highlighting a fundamental result in linear algebra: any symmetric matrix $A: \mathbb{R}^n \to \mathbb{R}^n$ possesses only real eigenvalues and is diagonalizable. Furthermore, its eigenvectors form an orthonormal basis for $\mathbb{R}^n$. This concept, known as the **Theorem of Principal Axes** (for standard scalar product), states that for every symmetric real matrix $A: \mathbb{R}^n \to \mathbb{R}^n$, there exists an orthonormal basis of $\mathbb{R}^n$ composed of eigenvectors of $A$. This theorem is foundational, as it shows that symmetric matrices map a unit sphere to an ellipsoid.

As a direct consequence of this theorem, we can derive the powerful [Singular Value Decomposition (SVD)](https://felwiki.basta.one/en/Concepts/singular-value-decomposition-svd_mc_singular-value-decomposition-svd). The SVD theorem asserts that any matrix $M: \mathbb{R}^s \to \mathbb{R}^r$ can be uniquely decomposed into the form:

$$M = USV^T$$

Here, $U: \mathbb{R}^r \to \mathbb{R}^r$ and $V: \mathbb{R}^s \to \mathbb{R}^s$ are [orthogonal matrices](https://felwiki.basta.one/en/Concepts/orthogonal-matrix_mc_orthogonal-matrix), meaning their transposes are equal to their inverses ($U^T = U^{-1}$ and $V^T = V^{-1}$). The matrix $S: \mathbb{R}^s \to \mathbb{R}^r$ is a "diagonal" matrix whose main diagonal contains non-negative real numbers known as [Singular Values (σ)](https://felwiki.basta.one/en/Concepts/singular-values_mc_singular-values-σ), typically ordered from largest to smallest: $\sigma_1 \ge \sigma_2 \ge \dots \ge \sigma_h > 0$, where $h = \text{rank}(M)$. All other entries in $S$ are zero. The singular values are, in fact, the square roots of the eigenvalues of the symmetric matrix $M^TM$.

For example, for the matrix $M = [[14, 4, 11], [-2, 8, 7]]$, its SVD involves computing $M^TM$ and finding its eigenvalues and eigenvectors. The eigenvalues of $M^TM$ are $\lambda_1 = 360$, $\lambda_2 = 90$, and $\lambda_3 = 0$. Consequently, the [Singular Values (σ)](https://felwiki.basta.one/en/Concepts/singular-values_mc_singular-values-σ) of $M$ are $\sigma_1 = \sqrt{360} = 6\sqrt{10}$ and $\sigma_2 = \sqrt{90} = 3\sqrt{10}$. The full SVD of $M$ can then be constructed using these singular values and the orthonormal bases $U$ and $V$.

### Geometric Interpretation of SVD

The [Singular Value Decomposition (SVD)](https://felwiki.basta.one/en/Concepts/singular-value-decomposition-svd_mc_singular-value-decomposition-svd) has a beautiful geometric interpretation. The transformation $x \mapsto Mx$ can be understood as a sequence of three fundamental geometric operations:
1.  **Rotation (or reflection) by $V^T$**: The input vector space $\mathbb{R}^s$ is rotated (or reflected) by the [orthogonal matrix](https://felwiki.basta.one/en/Concepts/orthogonal-matrix_mc_orthogonal-matrix) $V^T$.
2.  **Scaling by $S$**: The resulting vectors are then scaled along the principal axes, and possibly mapped to a different dimension, by the diagonal matrix $S$. This transformation converts a unit sphere into an ellipsoid, potentially degenerated (flattened along certain axes if singular values are zero).
3.  **Rotation (or reflection) by $U$**: Finally, the ellipsoid is rotated (or reflected) by the [orthogonal matrix](https://felwiki.basta.one/en/Concepts/orthogonal-matrix_mc_orthogonal-matrix) $U$ in the output vector space $\mathbb{R}^r$.

Essentially, the SVD represents any linear transformation as a rotation, followed by a scaling, followed by another rotation. This provides new orthonormal bases in $\mathbb{R}^s$ and $\mathbb{R}^r$ where the matrix $M$ acts purely as a scaling transformation.

### SVD for Data Compression and Approximation

One of the most significant applications of [Singular Value Decomposition (SVD)](https://felwiki.basta.one/en/Concepts/singular-value-decomposition-svd_mc_singular-value-decomposition-svd) is in [Data Compression (using SVD)](https://felwiki.basta.one/en/Concepts/data-compression-using-svd_mc_data-compression-using-svd) and low-rank matrix approximation. A full SVD decomposition of a matrix $M$ with rank $h$ can be expressed as a sum of outer products:

$$M = \sum_{j=1}^h \sigma_j u_j v_j^T$$

where $u_j$ are the columns of $U$ and $v_j$ are the columns of $V$. By taking a partial sum, $M_k = \sum_{j=1}^k \sigma_j u_j v_j^T$ for $k \le h$, we obtain a rank-$k$ approximation of $M$. This approximation $M_k$ is the best possible rank-$k$ approximation in terms of the [Frobenius Norm (||.||F)](https://felwiki.basta.one/en/Concepts/frobenius-norm-.-f_mc_frobenius-norm-f.md). The [Frobenius Norm (||.||F)](https://felwiki.basta.one/en/Concepts/frobenius-norm-.-f_mc_frobenius-norm-f.md) of a matrix $X$ is defined as:

$$||X||_F = \sqrt{\sum_{j=1}^s \sum_{i=1}^r x_{ij}^2}$$

The error of this approximation, measured by the [Frobenius Norm (||.||F)](https://felwiki.basta.one/en/Concepts/frobenius-norm-.-f_mc_frobenius-norm-f.md) of the difference, is given by:

$$||M - M_k||_F = \sqrt{\sigma_{k+1}^2 + \dots + \sigma_h^2}$$

And the total [Frobenius Norm (||.||F)](https://felwiki.basta.one/en/Concepts/frobenius-norm-.-f_mc_frobenius-norm-f.md) of $M$ is $||M||_F = \sqrt{\sigma_1^2 + \dots + \sigma_h^2}$. The relative change (or error) when approximating $M$ with $M_k$ is:

$$\frac{||M - M_k||_F}{||M||_F} = \sqrt{\frac{\sigma_{k+1}^2 + \dots + \sigma_h^2}{\sigma_1^2 + \dots + \sigma_h^2}}$$

This property is highly valuable for [Data Compression (using SVD)](https://felwiki.basta.one/en/Concepts/data-compression-using-svd_mc_data-compression-using-svd), especially for images. By keeping only the largest singular values, we can reconstruct a highly accurate approximation of the original image using significantly less data. For instance, an $8 \times 8$ pixel image example showed that using only the top 4 singular values resulted in a perfect reconstruction, as the remaining singular values were zero. Even with fewer singular values (e.g., 1, 2, or 3), the image quickly becomes recognizable, demonstrating the efficiency of this compression method.

### The Pseudoinverse and its Calculation via SVD

A significant portion of the lecture focused on addressing the challenge of matrix inversion when a matrix is not square or is singular. For such matrices, the standard inverse does not exist. This leads to the concept of the [Pseudoinverse (Moore-Penrose inverse)](https://felwiki.basta.one/en/Concepts/pseudoinverse-moore-penrose-inverse_mc_pseudoinverse-moore-penrose-inverse).

For any matrix $A: \mathbb{R}^s \to \mathbb{R}^r$, there exists a unique matrix $A^+: \mathbb{R}^r \to \mathbb{R}^s$, called the [Pseudoinverse (Moore-Penrose inverse)](https://felwiki.basta.one/en/Concepts/pseudoinverse-moore-penrose-inverse_mc_pseudoinverse-moore-penrose-inverse) of $A$, which satisfies the four Moore-Penrose conditions:
1.  $AA^+A = A$
2.  $A^+AA^+ = A^+$
3.  $(A^+A)^T = A^+A$
4.  $(AA^+)^T = AA^+$

Examples of pseudoinverses include:
*   For a regular matrix $A: \mathbb{R}^n \to \mathbb{R}^n$, its pseudoinverse is simply its inverse: $A^+ = A^{-1}$.
*   For a zero matrix $O^{s,r}: \mathbb{R}^s \to \mathbb{R}^r$, its pseudoinverse is the transposed zero matrix: $(O^{s,r})^+ = O^{r,s}$.
*   If $A: \mathbb{R}^k \to \mathbb{R}^n$ has rank $k$ (i.e., its columns are linearly independent), then $A^+ = (A^TA)^{-1}A^T$. Notably, in this case, $AA^+b$ represents the [Orthogonal Projection](https://felwiki.basta.one/en/Concepts/orthogonal-projection_mc_orthogonal-projection.md) of vector $b$ onto the image space of $A$, which aligns with the conceptual motivation for the pseudoinverse.

The lecture then unveiled the most general method for finding the [Pseudoinverse (Moore-Penrose inverse)](https://felwiki.basta.one/en/Concepts/pseudoinverse-moore-penrose-inverse_mc_pseudoinverse-moore-penrose-inverse) of a matrix, which relies on its [Singular Value Decomposition (SVD)](https://felwiki.basta.one/en/Concepts/singular-value-decomposition-svd_mc_singular-value-decomposition-svd). If $A = USV^T$ is the full SVD of matrix $A$, then:
*   The pseudoinverse of the diagonal matrix $S$ is $S^+ = \text{diag}(\frac{1}{\sigma_1}, \dots, \frac{1}{\sigma_h}, 0, \dots, 0)$, where $\sigma_j$ are the non-zero [Singular Values (σ)](https://felwiki.basta.one/en/Concepts/singular-values_mc_singular-values-σ) and the remaining diagonal entries are zero.
*   The pseudoinverse of matrix $A$ is given by:

    $$A^+ = VS^+U^T$$

This elegant formula provides a robust way to compute the pseudoinverse for any matrix, regardless of its shape or rank. The example matrix $M = [[14, 4, 11], [-2, 8, 7]]$ from earlier was used to demonstrate this, resulting in $M^+ = \frac{1}{180} [[10, -10], [7, 13], [4, 8]]$.

### Further Applications

Beyond data compression and solving non-invertible matrix problems, [Singular Value Decomposition (SVD)](https://felwiki.basta.one/en/Concepts/singular-value-decomposition-svd_mc_singular-value-decomposition-svd) and the [Pseudoinverse (Moore-Penrose inverse)](https://felwiki.basta.one/en/Concepts/pseudoinverse-moore-penrose-inverse_mc_pseudoinverse-moore-penrose-inverse) have numerous other applications:
*   **[Method of Least Squares](https://felwiki.basta.one/en/Concepts/method-of-least-squares_mc_method-of-least-squares.md)**: The pseudoinverse is central to finding the "best fit" solution to overdetermined or underdetermined systems of linear equations, minimizing the quadratic error.
*   **[Latent Semantic Indexing (LSI)](https://felwiki.basta.one/en/Concepts/latent-semantic-indexing-lsi_mc_latent-semantic-indexing-lsi.md)**: Used in information retrieval and natural language processing to uncover hidden semantic relationships between terms and documents by creating a vector model and applying SVD.
*   **[Principal Component Analysis (PCA)](https://felwiki.basta.one/en/Concepts/principal-component-analysis-pca_mc_principal-component-analysis-pca.md)**: A dimensionality reduction technique that uses SVD to identify the principal components (directions of greatest variance) in high-dimensional data, revealing essential measured quantities.

In conclusion, the lecture thoroughly explained the [Singular Value Decomposition (SVD)](https://felwiki.basta.one/en/Concepts/singular-value-decomposition-svd_mc_singular-value-decomposition-svd) as a powerful matrix factorization technique, elucidating its geometric meaning and demonstrating its practical utility in areas like [Data Compression (using SVD)](https://felwiki.basta.one/en/Concepts/data-compression-using-svd_mc_data-compression-using-svd). Furthermore, it introduced the indispensable concept of the [Pseudoinverse (Moore-Penrose inverse)](https://felwiki.basta.one/en/Concepts/pseudoinverse-moore-penrose-inverse_mc_pseudoinverse-moore-penrose-inverse), detailing its defining properties and, crucially, providing a method for its computation using SVD. This understanding of SVD and the pseudoinverse is vital for advanced topics in linear algebra and its widespread applications in science and engineering.

### Keywords
SVD, Singular Value Decomposition, Pseudoinverse, Linear Algebra, Data Compression