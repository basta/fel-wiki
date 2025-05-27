# Jordanův tvar

## Lineární algebra - Lecture 1

**Speaker:** Jiří Velebil

This lecture, delivered by Jiří Velebil, delves into the fundamental concept of the [Jordanův tvar](https://felwiki.basta.one/en/Concepts/jordan-v-tvar) (Jordan canonical form) in Linear Algebra. The primary goal is to provide a comprehensive method for representing linear transformations and matrices, particularly those that cannot be diagonalized. The lecture explains how any linear transformation can be decomposed into a sum of a diagonalizable part and a [nilpotentní zobrazení](https://felwiki.basta.one/en/Concepts/nilpotentn-zobrazen) that commute with each other. This decomposition, often referred to as the [Jordan-Chevalley Decomposition](https://felwiki.basta.one/en/Concepts/jordan-chevalley-decomposition), simplifies complex matrix operations and offers profound insights into the structure of linear operators.

### Motivation for Jordan Form: Beyond Diagonalization

Previous lectures covered the diagonalization of matrices for certain linear transformations between finite-dimensional spaces. However, not all matrices can be diagonalized. This lecture addresses such cases by introducing the [Jordanův tvar](https://felwiki.basta.one/en/Concepts/jordan-v-tvar), which provides an "almost diagonal" representation.

The concept of a [direktní rozklad](https://felwiki.basta.one/en/Concepts/direktn-rozklad) of a linear space and linear transformation is crucial here. For instance, a rotation in the $xy$-plane extended to $\mathbb{R}^3$ by fixing the $z$-axis can be viewed as a direct decomposition of $\mathbb{R}^3$ into the $xy$-plane ($\text{span}(e_1, e_2)$) and the $z$-axis ($\text{span}(e_3)$). Both of these subspaces are [invariantní podprostor](https://felwiki.basta.one/en/Concepts/invariantn-podprostor) under the given transformation.

For a [diagonalisovatelná matice](https://felwiki.basta.one/en/Concepts/diagonalisovateln-matice) $A: F^n \to F^n$, the space $F^n$ can be expressed as a [direktní rozklad](https://felwiki.basta.one/en/Concepts/direktn-rozklad) of the eigenspaces corresponding to distinct [vlastní hodnota](https://felwiki.basta.one/en/Concepts/vlastn-hodnota)s. For example, if $A = \begin{pmatrix} 5 & -2 & 2 \\ -1 & 4 & -1 \\ -4 & 4 & -1 \end{pmatrix}$, its [charakteristický polynom](https://felwiki.basta.one/en/Concepts/charakteristick-polynom-characteristic-polynomial) is $\text{char}_A(x) = -(x-3)^2(x-2)$. The [vlastní podprostor](https://felwiki.basta.one/en/Concepts/vlastn-podprostor-eigenspace) for $\lambda=3$ is $\text{span}(\begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix}, \begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix})$ and for $\lambda=2$ is $\text{span}(\begin{pmatrix} -2 \\ 1 \\ 4 \end{pmatrix})$. In this case, $\mathbb{R}^3 = \text{eigen}(3,A) \oplus \text{eigen}(2,A)$, and $A$ is similar to a block [diagonální matice](https://felwiki.basta.one/en/Concepts/diagon-ln-matice):
$$A \approx \begin{pmatrix} 3 & 0 \\ 0 & 3 \end{pmatrix} \oplus \begin{pmatrix} 2 \end{pmatrix}$$
This means $A$ is diagonalizable.

However, a matrix cannot be diagonalized if the dimension of an [invariantní podprostor](https://felwiki.basta.one/en/Concepts/invariantn-podprostor) corresponding to an [vlastní hodnota](https://felwiki.basta.one/en/Concepts/vlastn-hodnota) is less than its algebraic multiplicity. For instance, consider matrix $B = \begin{pmatrix} 2 & 4 & -3 \\ -1 & 10 & -6 \\ -1 & 8 & -4 \end{pmatrix}$, which has the same [charakteristický polynom](https://felwiki.basta.one/en/Concepts/charakteristick-polynom-characteristic-polynomial) as $A$, $\text{char}_B(x) = -(x-3)^2(x-2)$. Yet, its eigenspace for $\lambda=3$ is $\text{span}(\begin{pmatrix} 1 \\ 1 \\ 1 \end{pmatrix})$ and for $\lambda=2$ is $\text{span}(\begin{pmatrix} 0 \\ 3 \\ 4 \end{pmatrix})$. Since $\text{dim}(\text{eigen}(3,B)) = 1 < 2$ (the algebraic multiplicity of $\lambda=3$), $\mathbb{R}^3 \neq \text{eigen}(3,B) \oplus \text{eigen}(2,B)$, meaning $B$ is a [nediagonalisovatelná matice](https://felwiki.basta.one/en/Concepts/nediagonalisovateln-matice). The [Jordanův tvar](https://felwiki.basta.one/en/Concepts/jordan-v-tvar) provides a solution for such cases.

### The Essence of Jordan Form: Diagonal and Nilpotent Decomposition

The central idea of the [Jordanův tvar](https://felwiki.basta.one/en/Concepts/jordan-v-tvar) is to decompose a linear transformation $f$ (or its matrix $M$) into two commuting parts: a diagonalizable part ($f_{\text{diag}}$) and a [nilpotentní zobrazení](https://felwiki.basta.one/en/Concepts/nilpotentn-zobrazen) ($f_{\text{nil}}$):
$$f = f_{\text{diag}} + f_{\text{nil}}$$
where $f_{\text{nil}}$ is "almost zero" in the sense that $(f_{\text{nil}})^k = o$ (the zero transformation) for some integer $k$, and crucially, $f_{\text{nil}} \cdot f_{\text{diag}} = f_{\text{diag}} \cdot f_{\text{nil}}$. The smallest such $k$ is called the [index nilpotence](https://felwiki.basta.one/en/Concepts/index-nilpotence), denoted $\text{nil}(f)$.

An example of a [nilpotentní zobrazení](https://felwiki.basta.one/en/Concepts/nilpotentn-zobrazen) is the matrix $N = \begin{pmatrix} 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix}$. Its [index nilpotence](https://felwiki.basta.one/en/Concepts/index-nilpotence) is 3, because $N^3$ is the zero matrix. We can trace the action of $N$ on the canonical basis vectors:
$e_1 \to o$
$e_2 \to e_1 \to o$
$e_3 \to e_2 \to e_1 \to o$
$e_4 \to o$
The longest chain before reaching the zero vector determines the [index nilpotence](https://felwiki.basta.one/en/Concepts/index-nilpotence).

A special type of nilpotent matrix is the [Jordanova buňka](https://felwiki.basta.one/en/Concepts/jordanova-bu-ka) with $\lambda=0$. A general [Jordanova buňka](https://felwiki.basta.one/en/Concepts/jordanova-bu-ka) is a square matrix with a scalar $\lambda$ on the main diagonal, ones on the superdiagonal, and zeros elsewhere. Its dimension is equal to its [index nilpotence](https://felwiki.basta.one/en/Concepts/index-nilpotence) if $\lambda=0$.

### Finding the Jordan Form of a Matrix

The procedure to find the [Jordanův tvar](https://felwiki.basta.one/en/Concepts/jordan-v-tvar) of a matrix $M: F^n \to F^n$ involves several steps:
1.  **Characteristic Polynomial:** Compute the [charakteristický polynom](https://felwiki.basta.one/en/Concepts/charakteristick-polynom-characteristic-polynomial) of $M$, $\text{char}_M(x)$. If it cannot be factored into linear terms over the field $F$ (e.g., if working over $\mathbb{R}$ and complex roots exist), the Jordan form does not exist over $F$.
2.  **Eigenvalues and Multiplicities:** If $\text{char}_M(x) = a \cdot (x - \lambda_1)^{m_1} \cdot \dots \cdot (x - \lambda_p)^{m_p}$, then the Jordan form exists. It will consist of $p$ [Jordanův segment](https://felwiki.basta.one/en/Concepts/jordan-v-segment)s, $B_i(\lambda_i)$, each of dimension $m_i \times m_i$.
3.  **Constructing Jordan Segments:** For each eigenvalue $\lambda_i$, form the nilpotent matrix $M - \lambda_i \cdot E_n$ and find its Jordan form, $N_i$. Then the corresponding [Jordanův segment](https://felwiki.basta.one/en/Concepts/jordan-v-segment) is $B_i(\lambda_i) = N_i + \lambda_i \cdot E_{m_i}$.
4.  **Block Diagonal Matrix:** The [Jordanův tvar](https://felwiki.basta.one/en/Concepts/jordan-v-tvar) of $M$ is then formed as a block diagonal matrix composed of these [Jordanův segment](https://felwiki.basta.one/en/Concepts/jordan-v-segment)s. This form exists if the [charakteristický polynom](https://felwiki.basta.one/en/Concepts/charakteristick-polynom-characteristic-polynomial) can be fully factored, and it results in the decomposition $M \approx M_{\text{diag}} + M_{\text{nil}}$, where $M_{\text{diag}}$ is diagonal, $M_{\text{nil}}$ is nilpotent, and $M_{\text{diag}} M_{\text{nil}} = M_{\text{nil}} M_{\text{diag}}$.

### Practical Significance: Calculating Matrix Functions

One of the most important applications of the [Jordanův tvar](https://felwiki.basta.one/en/Concepts/jordan-v-tvar) is in simplifying the computation of matrix functions, particularly the [Matrix Exponential](https://felwiki.basta.one/en/Concepts/matrix-exponential). The [Matrix Exponential](https://felwiki.basta.one/en/Concepts/matrix-exponential), defined as $\exp(X) = \sum_{n=0}^{\infty} \frac{X^n}{n!}$, is crucial for solving systems of linear differential equations.

If we know the [Jordanův tvar](https://felwiki.basta.one/en/Concepts/jordan-v-tvar) of a matrix $M$, say $M \approx M_{\text{diag}} + M_{\text{nil}}$, then due to the commutativity ($M_{\text{diag}} M_{\text{nil}} = M_{\text{nil}} M_{\text{diag}}$), we can calculate $\exp(tM)$ as:
$$\exp(tM) \approx \exp(tM_{\text{diag}} + tM_{\text{nil}}) = \exp(tM_{\text{diag}}) \exp(tM_{\text{nil}})$$
The exponential of a [diagonální matice](https://felwiki.basta.one/en/Concepts/diagon-ln-matice) is straightforward (just exponentiate the diagonal entries). The exponential of a [nilpotentní zobrazení](https://felwiki.basta.one/en/Concepts/nilpotentn-zobrazen) $M_{\text{nil}}$ is a finite sum (polynomial) because $(M_{\text{nil}})^k = o$ for some $k$, so the power series for $\exp(tM_{\text{nil}})$ truncates at $n=k-1$. This makes the [matrix-exponential-computation](https://felwiki.basta.one/en/Concepts/matrix-exponential-computation) significantly easier.

For example, consider the matrix $M = \begin{pmatrix} 5 & 4 & 0 & 0 & 4 & 3 \\ 2 & 3 & 1 & 0 & 5 & 1 \\ 0 & -1 & 2 & 0 & 2 & 0 \\ -8 & -8 & -1 & -12 & -12 & -7 \\ 0 & 0 & 0 & 0 & -1 & 0 \\ -8 & -8 & -1 & 0 & -9 & -5 \end{pmatrix}$. Its [charakteristický polynom](https://felwiki.basta.one/en/Concepts/charakteristick-polynom-characteristic-polynomial) is $\text{char}_M(x) = (x-2)^4(x+1)^2$.
This implies its [Jordanův tvar](https://felwiki.basta.one/en/Concepts/jordan-v-tvar) will have two [Jordanův segment](https://felwiki.basta.one/en/Concepts/jordan-v-segment)s:
*   $B_1(2)$, a $4 \times 4$ segment corresponding to $\lambda=2$ (algebraic multiplicity 4).
*   $B_2(-1)$, a $2 \times 2$ segment corresponding to $\lambda=-1$ (algebraic multiplicity 2).

The [Jordanův tvar](https://felwiki.basta.one/en/Concepts/jordan-v-tvar) of $M$ is then:
$$M \approx B_1(2) \oplus B_2(-1) = \begin{pmatrix} 2 & 1 & 0 & 0 & 0 & 0 \\ 0 & 2 & 1 & 0 & 0 & 0 \\ 0 & 0 & 2 & 0 & 0 & 0 \\ 0 & 0 & 0 & 2 & 0 & 0 \\ 0 & 0 & 0 & 0 & -1 & 0 \\ 0 & 0 & 0 & 0 & 0 & -1 \end{pmatrix}$$
From this, we can derive $tM_{\text{diag}}$ and $tM_{\text{nil}}$:
$$tM_{\text{diag}} = \begin{pmatrix} 2t & 0 & 0 & 0 & 0 & 0 \\ 0 & 2t & 0 & 0 & 0 & 0 \\ 0 & 0 & 2t & 0 & 0 & 0 \\ 0 & 0 & 0 & 2t & 0 & 0 \\ 0 & 0 & 0 & 0 & -t & 0 \\ 0 & 0 & 0 & 0 & 0 & -t \end{pmatrix}$$
$$tM_{\text{nil}} = \begin{pmatrix} 0 & t & 0 & 0 & 0 & 0 \\ 0 & 0 & t & 0 & 0 & 0 \\ 0 & 0 & 0 & t & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 0 \end{pmatrix}$$
The [index nilpotence](https://felwiki.basta.one/en/Concepts/index-nilpotence) of $M_{\text{nil}}$ is 3, so its exponential simplifies to:
$$\exp(tM_{\text{nil}}) = E_6 + tM_{\text{nil}} + \frac{t^2}{2}M_{\text{nil}}^2$$
This demonstrates the significant computational advantage offered by the [Jordanův tvar](https://felwiki.basta.one/en/Concepts/jordan-v-tvar) in practical applications. While finding the [Jordanova báze](https://felwiki.basta.one/en/Concepts/jordanova-b-ze) can be technical, understanding the conceptual decomposition and its implications is key.

### Keywords
Linear Algebra, Jordan Form, Nilpotent Matrices, Matrix Decomposition, Eigenvalues