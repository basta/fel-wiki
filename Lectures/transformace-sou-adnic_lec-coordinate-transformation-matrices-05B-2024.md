# Transformace souřadnic
## Lineární algebra - 05B-2024
**Přednášející:** Jiří Velebil

This lecture on Linear Algebra, specifically focusing on coordinate transformations, builds upon previous discussions of linear mappings and their matrix representations. The primary goal is to understand how to transform coordinates of vectors between different bases within a vector space, a process facilitated by the concept of a coordinate transformation matrix. This lecture also highlights the increasing importance of solving matrix systems in linear algebra problems and sets the stage for a conceptually clear approach to solving such systems in future lectures.

### Recalling Matrix Representation of Linear Transformations

Before delving into coordinate transformations, the lecture briefly revisited the concept of a matrix representing a [linear transformation](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen_mc_lineární-zobrazení). If we have a linear mapping $f: L_1 \to L_2$ between finite-dimensional vector spaces $L_1$ and $L_2$, with ordered bases $B = (b_1, \dots, b_s)$ for $L_1$ and $C = (c_1, \dots, c_r)$ for $L_2$, then the matrix $A_f$ has $r$ rows and $s$ columns. Crucially, the $j$-th column of $A_f$ is formed by the coordinates of the image of the $j$-th basis vector $b_j$ with respect to basis $C$, written as a column vector:

$$ \text{j-th column of } A_f = \text{coord}_C(f(b_j)) $$

This definition forms the bedrock for understanding how matrices encode linear operations.

### Defining the Coordinate Transformation Matrix

The core of this lecture introduces the [Matice transformace souřadnic](https://felwiki.basta.one/en/Concepts/matice-transformace-sou-adnic_mc_matice-transformace-souřadnic), denoted $T_{B \to C}$. This matrix allows us to convert the coordinates of a vector from one basis $B$ to another basis $C$ within the same vector space $L$. Given two ordered bases $B = (b_1, \dots, b_n)$ and $C = (c_1, \dots, c_n)$ for a space $L$, the transformation matrix $T_{B \to C}$ is defined such that its $j$-th column consists of the coordinates of the $j$-th basis vector from $B$, expressed in terms of basis $C$:

$$ \text{j-th column of } T_{B \to C} = \text{coord}_C(b_j) $$

The notation $T_{B \to C}$ signifies the transformation *from* basis $B$ *to* basis $C$.

### Fundamental Properties of Coordinate Transformation Matrices

Several key properties govern these transformation matrices, making them powerful tools in linear algebra:

1.  **Coordinate Transformation Formula:** For any vector $x$ in $L$, its coordinates in basis $C$ can be found by multiplying its coordinates in basis $B$ by the transformation matrix $T_{B \to C}$:
    $$ T_{B \to C} \cdot \text{coord}_B(x) = \text{coord}_C(x) $$
    This direct relationship is a fundamental utility of these matrices.

2.  **Regularity and Inverse:** A [Matice transformace souřadnic](https://felwiki.basta.one/en/Concepts/matice-transformace-sou-adnic_mc_matice-transformace-souřadnic) is always a [regulární matice](https://felwiki.basta.one/en/Concepts/regul-rn-matice_mc_regulární-matice) (invertible). This is because the identity mapping from $L$ to $L$ is an [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus_mc_isomorfismus). Consequently, its inverse facilitates the reverse transformation:
    $$ (T_{B \to C})^{-1} = T_{C \to B} $$

3.  **Identity Transformation:** Transforming coordinates from a basis to itself results in the identity matrix ($E_n$):
    $$ T_{B \to B} = E_n $$

4.  **Composition Property:** For three bases $B, C, D$ of the same space $L$, transformations can be composed:
    $$ T_{B \to D} = T_{C \to D} \cdot T_{B \to C} $$
    This property is analogous to the composition of linear transformations, where the matrices are multiplied in the reverse order of the transformations.

### Practical Applications and Computations

The lecture illustrated these concepts with several examples, demonstrating how to apply and compute coordinate transformation matrices.

**Example: Recalculating Polynomial Coordinates:**
To find the coordinates of a polynomial $p(x) = -3x^2 + 6x + 3$ in $R_{\le 3}[x]$ with respect to a non-standard basis $C = ((x-1)^3, (x-1)^2, x-1, 1)$, given its coordinates in the standard basis $B = (x^3, x^2, x, 1)$, we use the formula:
$$ \text{coord}_C(p(x)) = T_{B \to C} \cdot \text{coord}_B(p(x)) $$
Knowing $\text{coord}_B(p(x)) = [0, -3, 6, 3]^T$, the challenge reduces to finding $T_{B \to C}$. This often involves finding the inverse of $T_{C \to B}$, since $T_{B \to C} = (T_{C \to B})^{-1}$.

**Example: Linearity and Multiple Bases:**
For a linear combination of vectors like $4x + 12y + 3z$ where $x, y, z$ have known coordinates in different bases ($x$ in $B$, $y$ in $C$, $z$ in $D$), its coordinates in basis $B$ can be computed using transformation matrices:
$$ \text{coord}_B(4x + 12y + 3z) = 4 \cdot \text{coord}_B(x) + 12 \cdot T_{C \to B} \cdot \text{coord}_C(y) + 3 \cdot T_{D \to B} \cdot \text{coord}_D(z) $$

**Computational Approach using Canonical Basis:**
In vector spaces like $F^n$, it's often convenient to use the [kanonická báze](https://felwiki.basta.one/en/Concepts/kanonick-b-ze_mc_kanonická-báze) ($K_n$) as an intermediate step for calculations. The transformation matrix $T_{B \to C}$ can be computed as:
$$ T_{B \to C} = (T_{C \to K_n})^{-1} \cdot T_{B \to K_n} $$
The matrices $T_{B \to K_n}$ and $T_{C \to K_n}$ are simply formed by taking the basis vectors $b_j$ (or $c_j$) as columns. The inverse $(T_{C \to K_n})^{-1}$ can be found efficiently using [Gaussova eliminace](https://felwiki.basta.one/en/Concepts/gaussova-eliminace_mc_gaussova-eliminace) in a block form: $(M | E_n) \sim (E_n | M^{-1})$.

**Example: Finding a Basis from a Transformation Matrix:**
The lecture demonstrated how to find an unknown basis $C$ if a known basis $B$ and the transformation matrix $T_{B \to C}$ are provided. By leveraging the relationship $T_{C \to K_n} = T_{B \to K_n} \cdot (T_{B \to C})^{-1}$, we can compute the columns of $T_{C \to K_n}$, which directly form the vectors of basis $C$.

### Changing the Matrix of a Linear Transformation with Basis Change

A significant theorem presented was how the matrix representation of a [linear transformation](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen_mc_lineární-zobrazení) changes when the bases of the domain and codomain are altered. If $A_f$ is the matrix of $f: L_1 \to L_2$ with respect to bases $B$ and $C$, then its matrix $A_f'$ with respect to new bases $B'$ and $C'$ is given by:
$$ A_f' = T_{C' \leftarrow C} \cdot A_f \cdot T_{B \leftarrow B'} $$
This formula illustrates how transformations (represented by $T$ matrices) "sandwich" the original transformation matrix to convert it into the new basis representation.

A particularly important special case arises when $L_1 = L_2$, and the same basis change is applied to both the domain and codomain (i.e., $B=C$ and $B'=C'$). In this scenario, the matrix $A_f$ transforms to $T^{-1} \cdot A_f \cdot T$, where $T = T_{B' \leftarrow B}$ is the transformation matrix from the old basis $B$ to the new basis $B'$.

### Similar Matrices: A Powerful Concept

This leads directly to the definition of [podobné matice](https://felwiki.basta.one/en/Concepts/podobn-matice_mc_podobné-matice). Two square matrices $A$ and $B$ are said to be similar ($A \approx B$) if there exists a [regulární matice](https://felwiki.basta.one/en/Concepts/regul-rn-matice_mc_regulární-matice) $T$ such that $B = T^{-1} \cdot A \cdot T$.

The profound significance of similar matrices is that they represent the *same* [lineární zobrazení](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen_mc_lineární-zobrazení), just expressed with respect to *different* bases. This concept is crucial for understanding the intrinsic properties of linear transformations, particularly when it comes to finding [vlastní hodnota](https://felwiki.basta.one/en/Concepts/vlastn-hodnota_mc_vlastní-hodnota) (eigenvalues), which are invariant under such basis changes.

The lecture concluded with an insightful example of a linear transformation $f: R^2 \to R^2$ where $f([[1],[-1]]) = 2 \cdot [[1],[-1]]$ and $f([[1],[1]]) = (1/3) \cdot [[1],[1]]$. In the non-canonical basis $B = ([[1],[-1]], [[1],[1]])$, the matrix $A_f$ is simply diagonal:
$$ A_f = \begin{pmatrix} 2 & 0 \\ 0 & 1/3 \end{pmatrix} $$
This "clearer" matrix immediately reveals the geometric nature of the transformation: it scales vectors along specific axes (the directions of the basis vectors in $B$). In contrast, the matrix of the same transformation in the [kanonická báze](https://felwiki.basta.one/en/Concepts/kanonick-b-ze_mc_kanonická-báze) $K_2$ is more complex:
$$ B_f = \begin{pmatrix} 7/6 & -5/6 \\ -5/6 & 7/6 \end{pmatrix} $$
While $A_f \approx B_f$, the simpler diagonal form of $A_f$ in its "natural" basis (formed by the eigenvectors) provides immediate insight into the transformation's action, reinforcing the importance of choosing an appropriate basis.

### Key Takeaways

*   Solving matrix systems is an increasingly vital skill in linear algebra.
*   [Podobné matice](https://felwiki.basta.one/en/Concepts/podobn-matice_mc_podobné-matice) represent the same [lineární zobrazení](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen_mc_lineární-zobrazení) but viewed from different bases, which is fundamental for understanding eigenvalues.
*   Selecting a "clearer" or more suitable [báze](https://felwiki.basta.one/en/Concepts/b-ze-basis_mc_báze-basis) can significantly simplify the matrix of a linear transformation, often revealing its intrinsic geometric properties at a glance.

**Keywords:** Linear Algebra, Coordinate Transformation, Basis Change, Matrix Representation, Linear Mapping