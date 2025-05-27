# Algebra matic

## Lineární algebra - Lecture 4

**Speaker:** Jiří Velebil

This lecture provided a comprehensive introduction to fundamental matrix algebra, specifically focusing on the definitions and properties of matrix addition, scalar multiplication, and matrix multiplication. It built upon the previous lecture's discussion of [linear transformations](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen_mc_lineární-zobrazení) and their [matrix representation](https://felwiki.basta.one/en/Concepts/maticov-z-pis_mc_maticový-zápis), extending these concepts to include algebraic operations with matrices. The session also laid the groundwork for understanding the invertibility of matrices and the solvability of matrix equations, emphasizing their practical applications in various fields.

---

### Matrix Addition and Scalar Multiplication

The lecture began by defining the most basic algebraic operations for matrices, treating them as elements within the [linear space](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-t-lesem-f-linear-space-over-field-f-vector-space-over-field-f) Lin($F^s$, $F^r$), which represents all linear transformations from $F^s$ to $F^r$. A crucial reminder from the previous lecture was established: vectors from space $F^1$ are consistently written as columns.

The definition of [součet matic](https://felwiki.basta.one/en/Concepts/sou-et-matic_mc_součet-matic) (matrix addition) was introduced. For two matrices $A = (a_1, \dots, a_s)$ and $B = (b_1, \dots, b_s)$ (represented by their column vectors), their sum $A+B$ is a matrix whose columns are the sums of the corresponding column vectors:
$$A + B = (a_1 + b_1, \dots, a_s + b_s)$$
This immediately provides a component-wise rule: to add two matrices of the same dimensions, simply add their corresponding entries. It's vital to remember that matrix addition is **only defined for matrices of the same dimensions**. Adding matrices of different sizes is not defined.

Similarly, the [skalární násobek matice](https://felwiki.basta.one/en/Concepts/skal-rn-n-sobek-matice_mc_skalární-násobek-matice) (scalar multiplication) for a scalar $\alpha$ from field $F$ and a matrix $A = (a_1, \dots, a_s)$ is defined as:
$$\alpha \cdot A = (\alpha \cdot a_1, \dots, \alpha \cdot a_s)$$
Again, this translates to a simple component-wise operation: to multiply a matrix by a scalar, multiply every entry of the matrix by that scalar.

The [nulová matice](https://felwiki.basta.one/en/Concepts/nulov-matice_mc_nulová-matice), denoted $O_{s,r}$, was defined as the zero vector in the linear space Lin($F^s$, $F^r$). It is a matrix where all entries are zero. Furthermore, for any matrix A, there exists a unique [opačná matice](https://felwiki.basta.one/en/Concepts/opa-n-matice_mc_opačná-matice), denoted $-A$, such that $A + (-A) = O_{s,r}$.

Examples were provided to illustrate these operations in Lin($\mathbb{R}^3$, $\mathbb{R}^2$):
*   **Matrix Addition:**
    $$ \begin{bmatrix} 5 & 3 & 6 \\ -1 & 0 & 7 \end{bmatrix} + \begin{bmatrix} 2 & 5 & -2 \\ 1 & 4 & 3 \end{bmatrix} = \begin{bmatrix} 7 & 8 & 4 \\ 0 & 4 & 10 \end{bmatrix} $$
*   **Scalar Multiplication:**
    $$ -2 \cdot \begin{bmatrix} -3 & 1 & 2 \\ 2 & 6 & 4 \end{bmatrix} = \begin{bmatrix} 6 & -2 & -4 \\ -4 & -12 & -8 \end{bmatrix} $$
*   **Zero Matrix:**
    $$ O_{3,2} = \begin{bmatrix} 0 & 0 & 0 \\ 0 & 0 & 0 \end{bmatrix} $$

These operations adhere to standard properties of linear spaces, including associativity and commutativity for addition, existence of a zero element and additive inverse, and distributive and associative laws for scalar multiplication.

### Matrix Multiplication

Building upon the representation of linear transformations by matrices, the lecture introduced the [součin matic](https://felwiki.basta.one/en/Concepts/sou-in-matic_mc_součin-matic) (matrix product). Given a linear transformation $A: F^s \to F^p$ and another $B: F^p \to F^r$, their composition $B \circ A$ is a linear transformation from $F^s$ to $F^r$. The matrix product $B \cdot A$ represents this composite transformation.

The definition states that for matrices $A=(a_1, \dots, a_s)$ and $B$, the $j$-th column of the product $B \cdot A$ is obtained by multiplying matrix $B$ by the $j$-th column vector of $A$, i.e., $B \cdot a_j$. Thus, in column notation:
$$B \cdot A = (B \cdot a_1, \dots, B \cdot a_s)$$
A crucial "dimensional check" is derived from this definition: the number of rows of matrix A must be equal to the number of columns of matrix B for the product $B \cdot A$ to be defined. If $A$ is a $p \times s$ matrix and $B$ is an $r \times p$ matrix, the product $B \cdot A$ will be an $r \times s$ matrix.

The individual entries of the product matrix $C = B \cdot A$ are given by the formula:
$$c_{ij} = \sum_{k=1}^{p} b_{ik} \cdot a_{kj}$$
where $b_{ik}$ are entries of $B$ and $a_{kj}$ are entries of $A$.

The power of matrix multiplication in representing composite [linear transformations](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen-linear-mapping-transformation_mc_lineární-zobrazení-linear-mapping-transformation) was vividly demonstrated with examples in $\mathbb{R}^2$:
*   **Projection on x-axis:** $P_x = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$
*   **Rotation by angle $\alpha$:** $R_\alpha = \begin{bmatrix} \cos \alpha & -\sin \alpha \\ \sin \alpha & \cos \alpha \end{bmatrix}$

The lecture showed how the product $P_x \cdot R_\alpha$ corresponds to "first rotate by $\alpha$, then project onto the x-axis":
$$ \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} \cdot \begin{bmatrix} \cos \alpha & -\sin \alpha \\ \sin \alpha & \cos \alpha \end{bmatrix} = \begin{bmatrix} \cos \alpha & -\sin \alpha \\ 0 & 0 \end{bmatrix} $$
Conversely, $R_\alpha \cdot P_x$ represents "first project onto the x-axis, then rotate by $\alpha$":
$$ \begin{bmatrix} \cos \alpha & -\sin \alpha \\ \sin \alpha & \cos \alpha \end{bmatrix} \cdot \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} = \begin{bmatrix} \cos \alpha & 0 \\ \sin \alpha & 0 \end{bmatrix} $$
These examples clearly illustrate that matrix multiplication generally does **not** satisfy the [komutativní zákon (pro součin matic)](https://felwiki.basta.one/en/Concepts/komutativn-z-kon-pro-sou-in-matic_mc_komutativní-zákon-pro-součin-matic) ($B \cdot A \neq A \cdot B$), even when both products are defined.

A more complex example involved a reflection across a line forming an angle $\alpha$ with the x-axis. This transformation can be decomposed into a sequence of transformations: rotation by $-\alpha$, followed by a reflection across the x-axis, and finally rotation by $\alpha$. This composite transformation is represented by the matrix product:
$$ \begin{bmatrix} \cos \alpha & -\sin \alpha \\ \sin \alpha & \cos \alpha \end{bmatrix} \cdot \begin{bmatrix} 1 & 0 \\ 0 & -1 \end{bmatrix} \cdot \begin{bmatrix} \cos(-\alpha) & -\sin(-\alpha) \\ \sin(-\alpha) & \cos(-\alpha) \end{bmatrix} = \begin{bmatrix} \cos 2\alpha & -\sin 2\alpha \\ \sin 2\alpha & -\cos 2\alpha \end{bmatrix} $$

Regarding properties, matrix multiplication does satisfy the [asociativní zákon (pro součin matic)](https://felwiki.basta.one/en/Concepts/asociativn-z-kon-pro-sou-in-matic_mc_asociativní-zákon-pro-součin-matic): $C \cdot (B \cdot A) = (C \cdot B) \cdot A$, whenever the products are defined. This property is directly derived from the associativity of composing linear transformations.

The concept of the [jednotková matice](https://felwiki.basta.one/en/Concepts/jednotkov-matice_mc_jednotkov-matice) ($E_n$) was introduced as the matrix representation of the identity [linear transformation](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen_mc_lineární-zobrazení) on $F^n$. Defined as $E_n = (e_1, \dots, e_n)$ where $e_i$ are the canonical basis vectors, it acts as an identity element for matrix multiplication: for any matrix $A: F^s \to F^r$, it holds that $E_r \cdot A = A = A \cdot E_s$.

### Matrix Equations and Invertibility

The lecture concluded by exploring the solvability of matrix equations, demonstrating their connection to systems of linear equations and the concept of [invertibilní matice](https://felwiki.basta.one/en/Concepts/invertibiln-matice_mc_invertibiln-matice).

Consider the projection matrix $P_x = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$ in $\mathbb{R}^2$. The lecture investigated two types of problems:

1.  **Describing the Image:** Does a vector $x = [x_1, x_2]$ exist such that its projection onto the x-axis is $b = [1, 2]$?
    Solving $P_x \cdot x = b$ means $\begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} \begin{bmatrix} x_1 \\ x_2 \end{bmatrix} = \begin{bmatrix} x_1 \\ 0 \end{bmatrix}$. Since $\begin{bmatrix} x_1 \\ 0 \end{bmatrix} \neq \begin{bmatrix} 1 \\ 2 \end{bmatrix}$ (as the second component is 0 on the left but 2 on the right), no such vector $x$ exists. This implies that the system of equations $P_x \cdot x = b$ has no solution for $b = [1,2]$.

2.  **Describing the Pre-image (or Kernel):** For a vector $b = [3, 0]$, what are all vectors $x = [x_1, x_2]$ that project onto $b$?
    Solving $P_x \cdot x = b$ yields $\begin{bmatrix} x_1 \\ 0 \end{bmatrix} = \begin{bmatrix} 3 \\ 0 \end{bmatrix}$. This equation implies $x_1 = 3$, while $x_2$ can be any real number. The solution set is all vectors of the form $[3, x_2]$, which can also be written as $[3, 0] + \text{span}([0, 1])$. This demonstrates how solving matrix equations generalizes solving systems of linear equations.

Finally, the lecture addressed the question of matrix invertibility. A square matrix $A$ is [invertibilní matice](https://felwiki.basta.one/en/Concepts/invertibiln-matice_mc_invertibiln-matice) if there exist matrices $X$ and $Y$ such that $A \cdot X = E_n$ and $Y \cdot A = E_n$, where $E_n$ is the [jednotková matice](https://felwiki.basta.one/en/Concepts/jednotkov-matice_mc_jednotkov-matice). For the projection matrix $P_x = \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix}$, it was shown that no such matrices $A$ or $B$ exist that satisfy $P_x \cdot A = E_2$ or $B \cdot P_x = E_2$.
$$ \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} \cdot \begin{bmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{bmatrix} = \begin{bmatrix} a_{11} & a_{12} \\ 0 & 0 \end{bmatrix} \neq \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} $$
$$ \begin{bmatrix} b_{11} & b_{12} \\ b_{21} & b_{22} \end{bmatrix} \cdot \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} = \begin{bmatrix} b_{11} & 0 \\ b_{21} & 0 \end{bmatrix} \neq \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} $$
This demonstrates that even a non-zero square matrix does not guarantee invertibility. The solvability of general matrix equations like $A \cdot X = B$ and $Y \cdot A = C$ is a critical topic in linear algebra, as it represents a fundamental generalization of solving systems of linear equations.

---

### Key Takeaways

*   **Vector Notation:** Always write vectors from $F^1$ as columns.
*   **Matrix Dimensions:** Matrix addition requires matrices of the same dimensions.
*   **Element-wise Operations:** Matrix addition and scalar multiplication are performed element-wise.
*   **Matrix Multiplication:** The product $B \cdot A$ is defined if the number of columns in $B$ equals the number of rows in $A$. Matrix multiplication is generally **not commutative**.
*   **Invertibility:** A non-zero square matrix is not necessarily invertible.
*   **Further Study:** For detailed examples and deeper understanding, students are encouraged to review Chapters 2.1, 2.2, and 4 of the textbook "Abstraktní a konkrétní lineární algebra", specifically examples 4.1.6 and 4.2.9.

**Keywords:** Matrix Algebra, Linear Transformations, Matrix Operations, Matrix Multiplication, Linear Spaces