# Diagonalisace matic

## Lineární algebra - Course 08B-2024
This lecture was delivered by Jiří Velebil.

This lecture provided a comprehensive overview of [matrix diagonalization](https://felwiki.basta.one/en/Concepts/diagonalisace-matic-matrix-diagonalization), exploring its conditions, forms, and practical applications in various mathematical and scientific domains. The discussion primarily focused on square matrices over complex ($\mathbb{C}$) and real ($\mathbb{R}$) fields, highlighting the nuanced differences in diagonalizability between these fields. Key concepts such as [eigenvalues](https://felwiki.basta.one/en/Concepts/vlastn-hodnota_mc_vlastn-hodnota) and [eigenvectors](https://felwiki.basta.one/en/Concepts/vlastn-vektor_mc_vlastn-vektor) were revisited, and the lecture introduced the [Jordan Canonical Form](https://felwiki.basta.one/en/Concepts/jordan-v-tvar_mc_jordanův-tvar) for matrices that are not fully diagonalizable. Furthermore, two significant applications were demonstrated: solving [linear homogeneous recurrence relations](https://felwiki.basta.one/en/Concepts/line-rn-homogenn-rekurentn-rovnice_mc_line-rn-homogenn-rekurentn-rovnice) (illustrated by the Fibonacci sequence) and defining and calculating matrix functions, specifically the [matrix exponential](https://felwiki.basta.one/en/Concepts/exponenci-la-matice_mc_exponenci-la-matice). The overarching theme underscored the importance of diagonalizability in simplifying complex matrix operations.

The lecture began by recalling previous topics, including the fundamental concepts of [eigenvalues](https://felwiki.basta.one/en/Concepts/vlastn-hodnota_mc_vlastn-hodnota) and [eigenvectors](https://felwiki.basta.one/en/Concepts/vlastn-vektor_mc_vlastn-vektor) of linear transformations, and the theorem concerning the diagonalizability of square matrices over the complex field $\mathbb{C}$.

### Diagonalizability Over Complex and Real Fields

A crucial property for understanding diagonalizability over $\mathbb{C}$ is its [algebraic closedness](https://felwiki.basta.one/en/Concepts/algebraick-uzav-enost_mc_algebraick-uzav-enost). This means every polynomial $p(x)$ in $\mathbb{C}[x]$ of degree $n$ has exactly $n$ roots (when counted with multiplicities). This property is central to a key theorem: for a square [matrix](https://felwiki.basta.one/en/Concepts/matice_mc_matice) $A$ over $\mathbb{C}$, it is [diagonalizable](https://felwiki.basta.one/en/Concepts/diagonalisovatelnost-matic_mc_diagonalisovatelnost-matic) if and only if for every complex eigenvalue $\lambda$, its multiplicity as a root of the [characteristic polynomial](https://felwiki.basta.one/en/Concepts/charakteristick-polynom-characteristic-polynomial_mc_charakteristick-polynom-characteristic-polynomial) $\text{char}_A(x)$ is equal to the dimension of its [eigenspace](https://felwiki.basta.one/en/Concepts/vlastn-podprostor-eigenspace_mc_vlastn-podprostor-eigenspace), $\text{dim}(\text{eigen}(\lambda, A))$.

Several examples were presented to illustrate this. The [Pauli Matrices](https://felwiki.basta.one/en/Concepts/pauliho-matice_mc_pauliho-matice)—$X$, $Y$, and $Z$—are important 2x2 complex matrices used in quantum mechanics and quantum computing.
$$
X = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \quad Y = \begin{pmatrix} 0 & -i \\ i & 0 \end{pmatrix} \quad Z = \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}
$$
All these matrices are diagonalizable. For instance, matrix $Z$ is already diagonal. The characteristic polynomial for matrix $X$ is $\text{char}_X(x) = x^2 - 1 = (x-1)(x+1)$. Its [eigenvalues](https://felwiki.basta.one/en/Concepts/vlastn-hodnota_mc_vlastn-hodnota) are $\lambda_1 = 1$ with [eigenvector](https://felwiki.basta.one/en/Concepts/vlastn-vektor_mc_vlastn-vektor) $t_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}$, and $\lambda_2 = -1$ with [eigenvector](https://felwiki.basta.one/en/Concepts/vlastn-vektor_mc_vlastn-vektor) $t_2 = \begin{pmatrix} 1 \\ -1 \end{pmatrix}$. This implies $X$ is similar to $\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$. Similarly, matrix $Y$ also has $\text{char}_Y(x) = x^2 - 1 = (x-1)(x+1)$, with eigenvalues $\lambda_1 = 1$ (eigenvector $v_1 = \begin{pmatrix} -i \\ 1 \end{pmatrix}$) and $\lambda_2 = -1$ (eigenvector $v_2 = \begin{pmatrix} i \\ 1 \end{pmatrix}$).

Useful identities for Pauli matrices were also mentioned, involving the [Poisson bracket](https://felwiki.basta.one/en/Concepts/poissonova-z-vorka_mc_poissonova-z-vorka) $\{\sigma_j, \sigma_k\} = \sigma_j\sigma_k + \sigma_k\sigma_j$ and the [commutator](https://felwiki.basta.one/en/Concepts/komut-tor_mc_komutátor) $[\sigma_j, \sigma_k] = \sigma_j\sigma_k - \sigma_k\sigma_j$:
$$
\sigma_x^2 = \sigma_y^2 = \sigma_z^2 = -i\sigma_1\sigma_2\sigma_3 = E_2
$$
$$
\{\sigma_j, \sigma_k\} = 2\delta_{jk}E_2
$$
$$
[\sigma_j, \sigma_k] = \sum_{l=1}^3 2i\epsilon_{jkl}\sigma_l
$$

### The Jordan Canonical Form

When a matrix is not fully diagonalizable, particularly if its [characteristic polynomial](https://felwiki.basta.one/en/Concepts/charakteristick-polynom-characteristic-polynomial_mc_charakteristick-polynom-characteristic-polynomial) can be factored into linear terms (which is always true for matrices over $\mathbb{C}$), it can be transformed into a special "almost diagonalizable" form known as the [Jordan Canonical Form](https://felwiki.basta.one/en/Concepts/jordan-v-tvar_mc_jordanův-tvar). This form $J$ is a block diagonal matrix composed of [Jordan blocks](https://felwiki.basta.one/en/Concepts/jordanova-bu-ka_mc_jordanova-bu-ka) $J_i$. Each [Jordan block](https://felwiki.basta.one/en/Concepts/jordanova-bu-ka_mc_jordanova-bu-ka) $J_i$ has a single eigenvalue $\lambda_i$ on its diagonal and ones directly above the diagonal (on the superdiagonal), with zeros elsewhere. The size of a [Jordan block](https://felwiki.basta.one/en/Concepts/jordanova-bu-ka_mc_jordanova-bu-ka) corresponds to the multiplicity of its associated eigenvalue as a root of the characteristic polynomial. The existence and properties of the [Jordan Canonical Form](https://felwiki.basta.one/en/Concepts/jordan-v-tvar_mc_jordanův-tvar) will be further explored in subsequent lectures.

### Classification of Regular Transformations of the Plane

The lecture then examined the diagonalizability of matrices over the real field $\mathbb{R}$. Consider a [regular matrix](https://felwiki.basta.one/en/Concepts/regul-rn-matice-regular-matrix_mc_regulární-matice-regular-matrix) $A = \begin{pmatrix} a & -b \\ b & a \end{pmatrix}$ over $\mathbb{R}$. Its characteristic polynomial is $\text{char}_A(x) = (a-x)^2 + b^2 = x^2 - 2ax + (a^2 + b^2)$. The discriminant of this quadratic is $-4b^2$. Consequently, matrix $A$ is diagonalizable over $\mathbb{R}$ only if $b=0$. In this specific case, $A$ is already diagonal, $A = \begin{pmatrix} a & 0 \\ 0 & a \end{pmatrix}$, representing a uniform scaling (since $A$ is regular, $a \neq 0$).

If $b \neq 0$, the discriminant is negative, meaning $A$ is not diagonalizable over $\mathbb{R}$. However, when considered as a matrix over $\mathbb{C}$, $A$ has complex conjugate eigenvalues $\lambda_1 = a+bi$ and $\lambda_2 = a-bi$. By letting $r = |\lambda_1| = |\lambda_2| = \sqrt{a^2+b^2}$ and $\alpha$ be the argument of $a+bi$, the matrix $A$ can be expressed as a product of a scaling matrix and a [rotation](https://felwiki.basta.one/en/Concepts/rotace-rotation_mc_rotace-rotation) matrix:
$$
A = \begin{pmatrix} a & -b \\ b & a \end{pmatrix} = \begin{pmatrix} r & 0 \\ 0 & r \end{pmatrix} \begin{pmatrix} \cos \alpha & -\sin \alpha \\ \sin \alpha & \cos \alpha \end{pmatrix}
$$
This reveals that such a transformation is a [rotation](https://felwiki.basta.one/en/Concepts/rotace-rotation_mc_rotace-rotation) by angle $\alpha$ followed by a uniform [scaling](https://felwiki.basta.one/en/Concepts/zm-na-m-tka-scaling_mc_zm-na-m-tka-scaling) by factor $r$.

This analysis leads to a powerful classification of regular transformations of the plane without a 2-fold eigenvalue. Such transformations are either:
1.  Similar to a [diagonal matrix](https://felwiki.basta.one/en/Concepts/diagon-ln-matice_mc_diagonální-matice) $\begin{pmatrix} a & 0 \\ 0 & b \end{pmatrix}$ (where $a \neq b$ are real and non-zero), representing scaling with different factors along different axes.
2.  Similar to a matrix of the form $\begin{pmatrix} r & 0 \\ 0 & r \end{pmatrix} \begin{pmatrix} \cos \alpha & -\sin \alpha \\ \sin \alpha & \cos \alpha \end{pmatrix}$ (where $r > 0$ and $\alpha \in [0, 2\pi)$), representing a [rotation](https://felwiki.basta.basta.one/en/Concepts/rotace-rotation_mc_rotace-rotation) followed by a uniform [scaling](https://felwiki.basta.one/en/Concepts/zm-na-m-tka-scaling_mc_zm-na-m-tka-scaling).

The proof strategy involves considering two cases: if the matrix is diagonalizable over $\mathbb{R}$, it has two distinct real eigenvalues leading to the first type. If it's not diagonalizable over $\mathbb{R}$, its characteristic polynomial must have complex conjugate roots, allowing it to be transformed into the second form using the real and imaginary parts of its complex eigenvectors.

### Applications of Matrix Diagonalization

A significant advantage of [matrix diagonalization](https://felwiki.basta.one/en/Concepts/diagonalisace-matic-matrix-diagonalization) lies in simplifying the computation of matrix powers. If a [diagonalizable matrix](https://felwiki.basta.one/en/Concepts/diagonalisovatelnost-matic_mc_diagonalisovatelnost-matic) $A$ can be written as $A = T^{-1} D T$ for some [regular matrix](https://felwiki.basta.one/en/Concepts/regul-rn-matice-regular-matrix_mc_regulární-matice-regular-matrix) $T$ and [diagonal matrix](https://felwiki.basta.one/en/Concepts/diagon-ln-matice_mc_diagonální-matice) $D$, then its powers can be computed simply as:
$$
A^k = T^{-1} D^k T
$$
Since powers of a [diagonal matrix](https://felwiki.basta.one/en/Concepts/diagon-ln-matice_mc_diagonální-matice) are trivial to compute ($D^k$ is obtained by raising each diagonal element to the power $k$), this method vastly simplifies calculating $A^k$.

Two main applications of this principle were discussed:

#### Solving Linear Homogeneous Recurrence Relations
[Linear homogeneous recurrence relations](https://felwiki.basta.one/en/Concepts/line-rn-homogenn-rekurentn-rovnice_mc_line-rn-homogenn-rekurentn-rovnice) are equations that define a sequence where each term is a linear combination of previous terms. A prime example is the Fibonacci sequence, defined by $F(n+2) = F(n+1) + F(n)$ for $n \ge 0$. The goal is to find an explicit formula for $F(n)$.
This can be solved by constructing a generating [matrix](https://felwiki.basta.one/en/Concepts/matice_mc_matice) $F = \begin{pmatrix} 0 & 1 \\ 1 & 1 \end{pmatrix}$. We can then write:
$$
\begin{pmatrix} F(n) \\ F(n+1) \end{pmatrix} = F^n \begin{pmatrix} F(0) \\ F(1) \end{pmatrix}
$$
The [matrix](https://felwiki.basta.one/en/Concepts/matice_mc_matice) $F$ is [diagonalizable](https://felwiki.basta.one/en/Concepts/diagonalisovatelnost-matic_mc_diagonalisovatelnost-matic) over $\mathbb{R}$ with eigenvalues $\lambda_1 = \frac{1+\sqrt{5}}{2}$ and $\lambda_2 = \frac{1-\sqrt{5}}{2}$. By using the diagonalization $F^n = T D^n T^{-1}$, an explicit formula for $F(n)$ can be derived:
$$
F(n) = \frac{\lambda_1^n \lambda_2 - \lambda_2^n \lambda_1}{\lambda_2 - \lambda_1} F(0) + \frac{-\lambda_1^n + \lambda_2^n}{\lambda_2 - \lambda_1} F(1)
$$
This method is applicable to any $k$-th order [linear homogeneous recurrence relation](https://felwiki.basta.one/en/Concepts/line-rn-homogenn-rekurentn-rovnice_mc_line-rn-homogenn-rekurentn-rovnice) of the form $X(n+k) = a_1X(n+k-1) + \dots + a_kX(n)$, provided the generating [matrix](https://felwiki.basta.one/en/Concepts/matice_mc_matice) is [diagonalizable](https://felwiki.basta.one/en/Concepts/diagonalisovatelnost-matic_mc_diagonalisovatelnost-matic). This technique is vital for analyzing the complexity of recursive algorithms and has parallels in solving linear homogeneous differential equations.

#### Matrix Functions: The Matrix Exponential
The concept of functions of matrices, particularly the [matrix exponential](https://felwiki.basta.one/en/Concepts/exponenci-la-matice_mc_exponenci-la-matice), is crucial in various fields like physics, computer graphics, and quantum computing. For a square [diagonalizable matrix](https://felwiki.basta.one/en/Concepts/diagonalisovatelnost-matic_mc_diagonalisovatelnost-matic) $X = T^{-1} D T$, the [matrix exponential](https://felwiki.basta.one/en/Concepts/exponenci-la-matice_mc_exponenci-la-matice) $e^X$ is defined via its Taylor series expansion, similar to the scalar exponential function:
$$
e^X = \sum_{n=0}^{\infty} \frac{X^n}{n!}
$$
By substituting the diagonalization $X = T^{-1} D T$, the computation simplifies dramatically:
$$
e^X = \sum_{n=0}^{\infty} T^{-1} \frac{D^n}{n!} T = T^{-1} \left( \sum_{n=0}^{\infty} \frac{D^n}{n!} \right) T = T^{-1} e^D T
$$
For a [diagonal matrix](https://felwiki.basta.one/en/Concepts/diagon-ln-matice_mc_diagonální-matice) $D$, its exponential $e^D$ is simply another [diagonal matrix](https://felwiki.basta.one/en/Concepts/diagon-ln-matice_mc_diagonální-matice) where each diagonal element is the exponential of the corresponding element in $D$. This method can be generalized to any function $f(x)$ that has a Taylor series expansion.

In summary, the lecture demonstrated that [matrix diagonalization](https://felwiki.basta.one/en/Concepts/diagonalisace-matic-matrix-diagonalization) is a powerful tool in linear algebra, simplifying complex operations like raising matrices to powers and defining matrix functions. While not all matrices are diagonalizable, particularly over the real numbers, the [Jordan Canonical Form](https://felwiki.basta.one/en/Concepts/jordan-v-tvar_mc_jordanův-tvar) provides a nearly diagonal equivalent, showcasing the pervasive utility of these concepts across various applications.

### Keywords
Matrix Diagonalization, Linear Algebra, Eigenvalues, Eigenvectors, Jordan Canonical Form, Recurrence Relations, Matrix Functions