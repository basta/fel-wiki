# Matice ortogonální projekce a metoda nejmenších čtverců

## Lineární algebra - 11A-2024

**Přednášející:** Jiří Velebil

This lecture provides a comprehensive overview of orthogonal projection matrices and the powerful [method of least squares](https://felwiki.basta.one/en/Concepts/metoda-nejmen-ch-tverc-least-squares-method_mc_metoda-nejmenších-čtverců-least-squares-method.md), primarily focusing on applications within $\mathbb{R}^n$ equipped with the [standard scalar product](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in_mc_standardní-skalární-součin.md). The session aims to equip students with the theoretical understanding and practical skills to compute orthogonal projections and apply the least squares method to find approximate solutions to inconsistent linear systems, particularly in data fitting scenarios.

### Ortogonální projekce a rejekce

The lecture began by revisiting the fundamental concepts of orthogonal projection and rejection. For any vector $x$ in a linear space $L$ with a [scalar product](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in-scalar-product_mc_skalární-součin-scalar-product.md), and a subspace $W$, the [orthogonal projection](https://felwiki.basta.one/en/Concepts/ortogon-ln-projekce-orthogonal-projection_mc_ortogonální-projekce-orthogonal-projection.md) of $x$ onto $W$, denoted $proj_W(x)$, is defined as the vector in $W$ such that the difference $x - proj_W(x)$ is orthogonal to all vectors in $W$. This difference vector, $x - proj_W(x)$, is termed the [orthogonal rejection](https://felwiki.basta.one/en/Concepts/ortogon-ln-rejekce-orthogonal-rejection_mc_ortogonální-rejekce-orthogonal-rejection.md) of $x$ from $W$, denoted $rej_W(x)$.

A key property highlighting the importance of orthogonal rejection is its "shortest" nature. Building upon the [Pythagorean theorem](https://felwiki.basta.one/en/Concepts/pythagorova-v-ta_mc_pythagorova-věta.md), for any vector $x$ not in $W$ and any vector $w$ in $W$, the following inequality holds: $||x - proj_W(x)||^2 \leq ||x - w||^2$. This demonstrates that the orthogonal projection of $x$ onto $W$ is the closest vector in $W$ to $x$, making the orthogonal rejection the smallest possible error vector. This fundamental property forms the basis for the least squares method.

### Výpočet matice ortogonální projekce

A significant part of the lecture focused on computing the [matrix of orthogonal projection](https://felwiki.basta.one/en/Concepts/matice-ortogon-ln-projekce-orthogonal-projection-matrix_mc_matice-ortogonální-projekce-orthogonal-projection-matrix.md). While one approach involves first orthogonalizing a given basis using the [Gram-Schmidt process](https://felwiki.basta.one/en/Concepts/gram-schmidt-orthogonalization-process_mc_gram-schmidt-orthogonalization-process.md) and then applying the simpler formula for orthogonal bases, a more general formula is available.

For a subspace $W$ of $\mathbb{R}^n$ with a scalar product defined by a [metric tensor](https://felwiki.basta.one/en/Concepts/metrick-tensor_mc_metrický-tensor.md) $G$, and with $A = (a_1, \dots, a_k)$ being the matrix whose columns form *any* basis for $W$, the orthogonal projection of a vector $x$ onto $W$ is given by the formula:

$$proj_W(x) = A (A^T G A)^{-1} A^T G x$$

For the [standard scalar product](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in_mc_standardní-skalární-součin.md), where $G$ is the identity matrix $E_n$, this formula simplifies considerably to:

$$proj_W(x) = A (A^T A)^{-1} A^T x$$

The lecture provided examples to illustrate these calculations, including finding the projection matrix onto a plane in $\mathbb{R}^3$ with the standard scalar product, and onto a line in $\mathbb{R}^2$ with a non-standard scalar product defined by a specific [metric tensor G](https://felwiki.basta.one/en/Concepts/metrick-tensor-g-metric-tensor-g_mc_metrický-tensor-g-metric-tensor-g.md).

### Charakteristika matic ortogonálních projekcí

A crucial theorem presented characterizes [orthogonal projection matrices](https://felwiki.basta.one/en/Concepts/matice-ortogon-ln-projekce-orthogonal-projection-matrix_mc_matice-ortogonální-projekce-orthogonal-projection-matrix.md). For a matrix $P: \mathbb{R}^n \to \mathbb{R}^n$ and a scalar product defined by a [metric tensor G](https://felwiki.basta.one/en/Concepts/metrick-tensor-g-metric-tensor-g_mc_metrický-tensor-g-metric-tensor-g.md), $P$ is an orthogonal projection matrix onto its image (column space) $im(P)$ of dimension $k$ if and only if two conditions are met:
1.  $\text{rank}(P) = k$ and $P^2 = P$ (idempotence).
2.  $\langle Px \vert y \rangle = \langle x \vert Py \rangle$ (self-adjointness with respect to the scalar product).

For the [standard scalar product](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in_mc_standardní-skalární-součin.md) (where $G = E_n$), the second condition simplifies to $P^T = P$ (symmetry). Thus, for the standard scalar product, an orthogonal projection matrix is characterized by being idempotent and symmetric.

### Aplikace: Metoda nejmenších čtverců

The latter part of the lecture was dedicated to the core application of orthogonal projections: the [method of least squares](https://felwiki.basta.one/en/Concepts/metoda-nejmen-ch-tverc-least-squares-method_mc_metoda-nejmenších-čtverců-least-squares-method.md). This method is essential for finding the "best approximate" solution to a system of linear equations $Ax = b$ when no exact solution exists, meaning the system is inconsistent. This often occurs in real-world scenarios, such as when fitting a model to noisy data.

Consider the problem of fitting a straight line, $y = ax + b'$, to a set of data points $(x_i, y_i)$. If these points do not perfectly lie on a line, the corresponding system of equations will be inconsistent. The [method of least squares](https://felwiki.basta.one/en/Concepts/metoda-nejmen-ch-tverc-least-squares-method_mc_metoda-nejmenších-čtverců-least-squares-method.md) seeks to minimize the squared error (or residual sum of squares), $||b - Ax||^2$, where $x$ represents the unknown coefficients (e.g., $a$ and $b'$ for a line).

The solution $\hat{x}$ that minimizes this error is given by the normal equations: $A^T A \hat{x} = A^T b$. If the matrix $A$ has [linearly independent columns](https://felwiki.basta.one/en/Concepts/line-rn-nez-vislost_mc_lineární-nezávislost.md), then $A^T A$ is a [positive definite matrix](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice-positive-definite-matrix_mc_positivně-definitní-matice-positive-definite-matrix.md) and thus invertible, leading to the unique least squares solution:

$$\hat{x} = (A^T A)^{-1} A^T b$$

The vector $A\hat{x}$ is precisely the [orthogonal projection](https://felwiki.basta.one/en/Concepts/ortogon-ln-projekce-orthogonal-projection_mc_ortogonální-projekce-orthogonal-projection.md) of $b$ onto the column space of $A$, $im(A)$. This geometric interpretation confirms that $A\hat{x}$ is the closest vector in $im(A)$ to $b$, hence minimizing the distance $||b - A\hat{x}||$. This is why the squared error $||b - A\hat{x}||^2$ is the smallest possible.

The lecture illustrated this with an example of finding the "best fit" [regression line](https://felwiki.basta.one/en/Concepts/regresn-p-mka-regression-line_mc_regresní-přímka-regression-line.md) for three points not lying on a line, and further demonstrated its application to fitting a parabola $y = ax^2 + bx + c$ to data points. The matrix for such a system will have [linearly independent columns](https://felwiki.basta.one/en/Concepts/line-rn-nez-vislost_mc_lineární-nezávislost.md) if there are at least three distinct x-values.

Finally, the lecture touched upon the historical significance of the [method of least squares](https://felwiki.basta.one/en/Concepts/metoda-nejmen-ch-tverc-least-squares-method_mc_metoda-nejmenších-čtverců-least-squares-method.md), attributing its development to Carl Friedrich Gauss, who famously used it in 1801 to predict the orbit of the dwarf planet Ceres. This method forms the bedrock of regression analysis in mathematical statistics.

**Key Takeaways:**
*   **Orthogonal projection** finds the closest point in a subspace to a given vector, and its **rejection** quantifies the minimal error.
*   The [matrix of orthogonal projection](https://felwiki.basta.one/en/Concepts/matice-ortogon-ln-projekce-orthogonal-projection-matrix_mc_matice-ortogonální-projekce-orthogonal-projection-matrix.md) has specific properties ($P^2=P$ and self-adjointness/symmetry) for both general and [standard scalar products](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in_mc_standardní-skalární-součin.md).
*   The [method of least squares](https://felwiki.basta.one/en/Concepts/metoda-nejmen-ch-tverc-least-squares-method_mc_metoda-nejmenších-čtverců-least-squares-method.md) leverages orthogonal projections to find the optimal approximate solution to inconsistent linear systems by minimizing squared errors, which is crucial for applications like data fitting and regression.

### Keywords
Linear Algebra, Orthogonal Projection, Least Squares Method, Matrix Theory, Regression Analysis