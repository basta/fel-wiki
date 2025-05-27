# Charakterisace skalárních součinů v Rn

## Lineární algebra

This lecture, delivered by Jiří Velebil, delves into the essential characteristics of [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in)s in $\mathbb{R}^n$, focusing primarily on linear spaces over the real numbers. The core objective is to understand how these products are defined, how they relate to specific types of matrices, and how to construct them to achieve desired properties, such as making a given basis [ortonormální báze](https://felwiki.basta.one/en/Concepts/ortonorm-ln-b-ze).

### The Foundation: Scalar Products and Matrices

The lecture begins by revisiting familiar concepts of [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) in $\mathbb{R}^2$. The [standardní skalární součin](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in), often denoted as $\langle \mathbf{x} | \mathbf{y} \rangle_{std} = x_1y_1 + x_2y_2$, can be expressed as a matrix product: $(x_1, x_2) \cdot \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \cdot \begin{pmatrix} y_1 \\ y_2 \end{pmatrix}$.
A "non-standard" scalar product, such as $\langle \mathbf{x} | \mathbf{y} \rangle_{unusual} = x_1y_1 + x_2y_1 + x_1y_2 + 2x_2y_2$, can similarly be represented using a matrix: $(x_1, x_2) \cdot \begin{pmatrix} 1 & 1 \\ 1 & 2 \end{pmatrix} \cdot \begin{pmatrix} y_1 \\ y_2 \end{pmatrix}$. This observation leads to a fundamental question: Is it a coincidence that these scalar products are defined by $2 \times 2$ matrices? The lecture emphatically states that it is not, paving the way for the central concept of [positivně definitní matice](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice).

### Characterizing Positive Definite Matrices

The lecture establishes that [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in)s in $\mathbb{R}^n$ correspond precisely to square matrices known as [positivně definitní matice](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice). A matrix $G$ of type $n \times n$ over $\mathbb{R}$ is defined as [positivně definitní](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice) if there exists a matrix $R$ with linearly independent columns such that $G = R^T R$. A crucial immediate consequence of this definition is that every [positivně definitní matice](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice) $G$ must be symmetric, since $G^T = (R^T R)^T = R^T (R^T)^T = R^T R = G$.

A key theorem provides several equivalent conditions for a real symmetric matrix $G$ to be [positivně definitní](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice):
1.  $G$ is [positivně definitní](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice).
2.  $G$ is symmetric, and the determinants of all leading principal minors (submatrices $G_k$, where $1 \leq k \leq n$) are positive. This condition is particularly useful in analysis for identifying local minima of multivariable functions.
3.  $G$ is symmetric, and the quadratic form $\mathbf{x}^T G \mathbf{x} > 0$ for all non-zero vectors $\mathbf{x} \in \mathbb{R}^n$ (equality holds only for $\mathbf{x} = \mathbf{o}$).
4.  $G$ is symmetric, and its characteristic polynomial $char_G(\lambda)$ has all real and positive roots (eigenvalues).
5.  There exists a [regulární matice](https://felwiki.basta.one/en/Concepts/regul-rn-matice) $R$ such that $G = R^T R$.

The lecture mentions that the proof for this comprehensive characterization theorem is complex and is omitted, encouraging interested students to consult the textbook (Theorem 12.3.4).

A related concept, the [Choleskyho faktorisace](https://felwiki.basta.one/en/Concepts/choleskyho-faktorisace), is briefly introduced as an optional topic. This factorization states that a matrix $G$ is [positivně definitní](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice) if and only if $G = R^T R$, where $R$ is a [regulární matice](https://felwiki.basta.one/en/Concepts/regul-rn-matice) in upper triangular form (also referred to as upper block form). An example of [Choleskyho faktorisace](https://felwiki.basta.one/en/Concepts/choleskyho-faktorisace) is given:
$$
\begin{pmatrix} 1 & 2 & 8 \\ 2 & 8 & 12 \\ 8 & 12 & 27 \end{pmatrix} = \begin{pmatrix} 1 & 2 & 3 \\ 0 & 2 & 3 \\ 0 & 0 & 3 \end{pmatrix}^T \cdot \begin{pmatrix} 1 & 2 & 3 \\ 0 & 2 & 3 \\ 0 & 0 & 3 \end{pmatrix}
$$

### The General Form of Scalar Products

The lecture culminates in a fundamental theorem describing the general form of a [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) in $\mathbb{R}^n$:
*   If $G$ is a [positivně definitní matice](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice) of type $n \times n$ over $\mathbb{R}$, then the matrix product $\mathbf{x}^T G \mathbf{y}$ defines a [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) in $\mathbb{R}^n$.
*   Conversely, every [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) $\langle - | - \rangle$ in $\mathbb{R}^n$ defines a unique [positivně definitní matice](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice) $G = (g_{ij})_{i,j=1}^n$, where $g_{ij} = \langle \mathbf{e}_i | \mathbf{e}_j \rangle$ (with $\mathbf{e}_i$ being the canonical basis vectors). This means we can always write $\langle \mathbf{x} | \mathbf{y} \rangle = \mathbf{x}^T G \mathbf{y}$.

The matrix $G$ is referred to as the [metrický tensor](https://felwiki.basta.one/en/Concepts/metrick-tensor) (or [Gramova matice](https://felwiki.basta.one/en/Concepts/gramova-matice)) of the [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in). Examples include the identity matrix $E_n$, which is [positivně definitní](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice) ($E_n = E_n^T E_n$), and defines the [standardní skalární součin](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in). The "unusual" $2 \times 2$ matrix from earlier, $G = \begin{pmatrix} 1 & 1 \\ 1 & 2 \end{pmatrix}$, is also confirmed as [positivně definitní](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice) because it is symmetric, and its principal minors are positive: $\det(G_1) = \det(1) = 1 > 0$ and $\det(G_2) = \det(G) = 1 \cdot 2 - 1 \cdot 1 = 1 > 0$.

For $\mathbb{R}^2$, a matrix $G = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$ defines a [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) if and only if it is symmetric ($c=b$), $a > 0$, and $ad - b^2 > 0$. This means the expression $ax_1y_1 + b(x_1y_2 + x_2y_1) + dx_2y_2$ defines a [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) if and only if these conditions hold.

### Geometric Interpretations: The Unit Circle

The lecture further explores the geometric implications of different [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in)s by examining the [jednotková kružnice](https://felwiki.basta.one/en/Concepts/jednotkov-kru-nice) in $\mathbb{R}^2$. For a [positivně definitní matice](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice) $G = \begin{pmatrix} a & b \\ b & d \end{pmatrix}$ and its corresponding [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in), the set of vectors $\mathbf{x} = (x_1, x_2)^T$ such that $||\mathbf{x}|| = 1$ (where $||\mathbf{x}|| = \sqrt{\langle \mathbf{x} | \mathbf{x} \rangle}$) forms the [jednotková kružnice](https://felwiki.basta.one/en/Concepts/jednotkov-kru-nice). The equation for this "circle" is $ax_1^2 + 2bx_1x_2 + dx_2^2 = 1$. The lecture shows that in the basis of eigenvectors of $G$, this equation always describes an ellipse. The nature of this ellipse (e.g., circular if $a=d$ and $b=0$) depends on the eigenvalues of $G$, which are guaranteed to be real and positive for a [positivně definitní matice](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice).

### Orthogonality, Norms, and Constructing Scalar Products

The lecture reiterates that every [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) induces a [norma](https://felwiki.basta.one/en/Concepts/norma). Key definitions are recalled:
*   [Ortogonální vektory](https://felwiki.basta.one/en/Concepts/ortogon-ln-vektory): $\mathbf{x}$ and $\mathbf{y}$ are [ortogonální](https://felwiki.basta.one/en/Concepts/ortogon-ln-vektory) if $\langle \mathbf{x} | \mathbf{y} \rangle = 0$.
*   [Norma](https://felwiki.basta.one/en/Concepts/norma) of $\mathbf{x}$: $||\mathbf{x}|| = \sqrt{\langle \mathbf{x} | \mathbf{x} \rangle}$.
*   [Normovaný vektor](https://felwiki.basta.one/en/Concepts/normovan-vektor): A vector $\mathbf{x}$ is [normovaný](https://felwiki.basta.one/en/Concepts/normovan-vektor) if $||\mathbf{x}|| = 1$.
*   [Ortonormální báze](https://felwiki.basta.one/en/Concepts/ortonorm-ln-b-ze): A basis where vectors are mutually [ortogonální](https://felwiki.basta.one/en/Concepts/ortogon-ln-vektory) and each is [normovaný](https://felwiki.basta.one/en/Concepts/normovan-vektor). For the [standardní skalární součin](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in) and the canonical basis $(\mathbf{e}_1, \dots, \mathbf{e}_n)$ in $\mathbb{R}^n$, $\langle \mathbf{e}_i | \mathbf{e}_j \rangle = \delta_{ij}$, illustrating the [Kronecker delta](https://felwiki.basta.one/en/Concepts/kronecker-delta) property of an [ortonormální báze](https://felwiki.basta.one/en/Concepts/ortonorm-ln-b-ze).

A significant result presented is that *any* ordered basis $(\mathbf{b}_1, \dots, \mathbf{b}_n)$ in $\mathbb{R}^n$ can be treated as an [ortonormální báze](https://felwiki.basta.one/en/Concepts/ortonorm-ln-b-ze) with respect to a *unique* [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in). This specific [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) satisfies $\langle \mathbf{b}_i | \mathbf{b}_j \rangle = \delta_{ij}$. The matrix $G$ for this unique [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) is constructed using the inverse of the change-of-basis matrix $T_{\mathcal{B} \leftarrow \mathcal{K}_n}$ (the matrix that transforms canonical coordinates to basis $\mathcal{B}$ coordinates). Specifically, $G = (T_{\mathcal{B} \leftarrow \mathcal{K}_n}^{-1})^T (T_{\mathcal{B} \leftarrow \mathcal{K}_n}^{-1})$.

An example is provided to illustrate this construction: finding a [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) in $\mathbb{R}^2$ such that vectors $(2, -3)^T$ and $(5, -3)^T$ are mutually [ortogonální](https://felwiki.basta.one/en/Concepts/ortogon-ln-vektory) and each has a [norma](https://felwiki.basta.one/en/Concepts/norma) of 1.
Given $\mathbf{b}_1 = (2, -3)^T$ and $\mathbf{b}_2 = (5, -3)^T$, the matrix $T_{\mathcal{B} \leftarrow \mathcal{K}_n} = \begin{pmatrix} 2 & 5 \\ -3 & -3 \end{pmatrix}$.
Its inverse is $T_{\mathcal{B} \leftarrow \mathcal{K}_n}^{-1} = \frac{1}{9} \begin{pmatrix} -3 & -5 \\ 3 & 2 \end{pmatrix}$.
The [metrický tensor](https://felwiki.basta.one/en/Concepts/metrick-tensor) $G$ is then calculated as:
$$
G = (T_{\mathcal{B} \leftarrow \mathcal{K}_n}^{-1})^T (T_{\mathcal{B} \leftarrow \mathcal{K}_n}^{-1}) = \frac{1}{81} \begin{pmatrix} -3 & 3 \\ -5 & 2 \end{pmatrix} \begin{pmatrix} -3 & -5 \\ 3 & 2 \end{pmatrix} = \frac{1}{81} \begin{pmatrix} 18 & 21 \\ 21 & 29 \end{pmatrix}
$$
This results in the [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in):
$$
\langle (x_1, x_2) | (y_1, y_2) \rangle = \frac{18}{81}x_1y_1 + \frac{21}{81}x_1y_2 + \frac{21}{81}x_2y_1 + \frac{29}{81}x_2y_2
$$
The lecture concludes this section by explaining the utility of such calculations: this particular [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) "sees" the chosen basis vectors as forming a [jednotková kružnice](https://felwiki.basta.one/en/Concepts/jednotkov-kru-nice) (specifically, a unit square grid), effectively transforming the geometry of the space relative to this inner product.

### Conclusion and Future Topics

This lecture provided a comprehensive understanding of [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in)s in $\mathbb{R}^n$, emphasizing their characterization through [positivně definitní matice](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice). It demonstrated how to define and identify such matrices and how to construct a [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) that makes any given basis an [ortonormální báze](https://felwiki.basta.one/en/Concepts/ortonorm-ln-b-ze).

The next lectures will build upon these concepts, focusing on processes to find a new [ortonormální báze](https://felwiki.basta.one/en/Concepts/ortonorm-ln-b-ze) from a given basis and a scalar product. This will involve the introduction of new fundamental concepts such as [ortogonální projekce](https://felwiki.basta.one/en/Concepts/ortogon-ln-projekce) and [ortogonální rejekce](https://felwiki.basta.one/en/Concepts/ortogon-ln-rejekce), which are crucial for techniques like the Gram-Schmidt orthogonalization process.

### Keywords
Linear Algebra, Scalar Products, Positive Definite Matrices, Orthonormal Basis, Cholesky Factorization