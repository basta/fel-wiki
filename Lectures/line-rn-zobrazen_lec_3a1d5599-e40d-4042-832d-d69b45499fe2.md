# Lineární zobrazení

## Lineární algebra (04A-2024) - Lecture 4
Presented by Jiří Velebil.

This lecture provides a fundamental introduction to linear transformations, defining them as special types of functions between vector spaces that preserve the underlying algebraic structure. It delves into how these transformations can be uniquely characterized and represented using matrices, particularly in the context of canonical bases. The session also explores various common geometric transformations in two-dimensional space and concludes by explaining how matrix-vector multiplication directly relates to the application of a linear transformation and the formulation of systems of linear equations.

### Defining Linear Transformations

The lecture began by formalizing the concept of a [lineární zobrazení](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen-linear-transformation_mc_lineární-zobrazení-linear-transformation) (linear mapping or transformation). A function $f: L_1 \to L_2$ between two vector spaces $L_1$ and $L_2$ (over the same field $F$) is defined as linear if it satisfies two conditions for all vectors $x, y \in L_1$ and all scalars $a \in F$:
1.  **Additivity:** $f(x+y) = f(x) + f(y)$
2.  **Homogeneity:** $f(a \cdot x) = a \cdot f(x)$

A crucial consequence of this definition is the [princip superposice](https://felwiki.basta.one/en/Concepts/princip-superposice-principle-of-superposition_mc_princip-superposice-principle-of-superposition), which states that a mapping $f: L_1 \to L_2$ is linear if and only if it preserves linear combinations:
$$f\left(\sum_{i=1}^{n} a_i \vec{x}_i\right) = \sum_{i=1}^{n} a_i f(\vec{x}_i)$$
This principle highlights the fundamental nature of linear transformations in preserving the structure of vector spaces. Furthermore, the set of all linear mappings from $L_1$ to $L_2$, denoted as Lin($L_1, L_2$), itself forms a linear space over the field $F$, implying that sums and scalar multiples of linear transformations are also linear.

### The Role of Bases in Defining Linear Transformations

A powerful theorem introduced in the lecture states that a [lineární zobrazení](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen-linear-transformation_mc_lineární-zobrazení-linear-transformation) is uniquely determined by its values on a [báze](https://felwiki.basta.one/en/Concepts/b-ze-basis_mc_báze-basis) of the domain space. This means that if you know where each basis vector of $L_1$ maps to in $L_2$, the entire linear mapping from $L_1$ to $L_2$ is completely specified. This principle is particularly useful for spaces with finite dimensions, where it simplifies the definition and analysis of linear maps.

### Representing Linear Transformations with Matrices

This foundational idea leads directly to the concept of a [matice](https://felwiki.basta.one/en/Concepts/matice_mc_matice). For linear transformations from $F^s$ to $F^r$, where $F^s$ is equipped with the [kanonická báze](https://felwiki.basta.one/en/Concepts/kanonick-b-ze-canonical-basis_mc_kanonická-báze-canonical-basis) $K_s = (e_1, \dots, e_s)$, specifying the linear transformation $f: F^s \to F^r$ is equivalent to specifying the images of the canonical basis vectors: $f(e_1) = a_1, \dots, f(e_s) = a_s$, where $a_j \in F^r$. These images, when arranged as columns, form the [matice](https://felwiki.basta.one/en/Concepts/matice_mc_matice) representing the linear transformation. An $r \times s$ matrix $A$ (with $r$ rows and $s$ columns) is therefore identified with the linear mapping $A: F^s \to F^r$ that maps each canonical basis vector $e_j$ to the $j$-th column vector $a_j$.

### Examples of Geometric Transformations in $\mathbb{R}^2$

The lecture provided several illustrative examples of common linear transformations in $\mathbb{R}^2$ and their corresponding matrix representations relative to the canonical basis $K_2 = (e_1, e_2)$. These examples provide intuitive understanding of how matrices encode geometric operations:

*   **[Projekce na osu x](https://felwiki.basta.one/en/Concepts/ortogon-ln-projekce_mc_ortogonální-projekce):** Maps a vector $(x, y)$ to $(x, 0)$.
    $$P_x = \begin{pmatrix} 1 & 0 \\ 0 & 0 \end{pmatrix}$$
*   **[Projekce na osu y](https://felwiki.basta.one/en/Concepts/ortogon-ln-projekce_mc_ortogonální-projekce):** Maps a vector $(x, y)$ to $(0, y)$.
    $$P_y = \begin{pmatrix} 0 & 0 \\ 0 & 1 \end{pmatrix}$$
*   **[Rotace](https://felwiki.basta.one/en/Concepts/rotace-rotation_mc_rotace-rotation) (by angle $\alpha$):** Rotates a vector counter-clockwise around the origin.
    $$R_\alpha = \begin{pmatrix} \cos \alpha & -\sin \alpha \\ \sin \alpha & \cos \alpha \end{pmatrix}$$
*   **[Změna měřítka](https://felwiki.basta.one/en/Concepts/zm-na-m-tka-scaling_mc_změna-měřítka-scaling):** Scales the x and y components by factors $a$ and $b$ respectively.
    $$\begin{pmatrix} a & 0 \\ 0 & b \end{pmatrix}$$
    A special case is [reflexe](https://felwiki.basta.one/en/Concepts/reflexe-reflection_mc_reflexe-reflection) (e.g., across the x-axis for $a=1, b=-1$):
    $$\begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix}$$
*   **[Zkosení](https://felwiki.basta.one/en/Concepts/zkosen-shear-transformation_mc_zkosení-shear-transformation) (Shear):** Shifts points in a direction parallel to an axis, proportional to their distance from that axis.
    $$S_{a,b} = \begin{pmatrix} 1 & b \\ a & 1 \end{pmatrix} \quad \text{where } a, b \in \mathbb{R}$$
    These types of shear transformations are particularly important for solving [systém lineárních rovnic](https://felwiki.basta.one/en/Concepts/syst-m-line-rn-ch-rovnic-system-of-linear-equations_mc_systém-lineárních-rovnic-system-of-linear-equations).

### Matrix-Vector Multiplication and Systems of Linear Equations

The lecture then elucidated the meaning of [násobení matice vektorem](https://felwiki.basta.one/en/Concepts/n-soben-matice-vektorem-matrix-vector-multiplication_mc_násobení-matice-vektorem-matrix-vector-multiplication). For a matrix $A: F^s \to F^r$ with columns $(a_1, \dots, a_s)$ and a vector $x = (x_1, \dots, x_s)^T \in F^s$, the application of the matrix $A$ to vector $x$ is defined as a linear combination of the matrix's column vectors, scaled by the components of $x$:
$$A : \vec{x} \mapsto \sum_{j=1}^{s} x_j \vec{a}_j$$
This result is conventionally denoted as $A \cdot x$. An example demonstrating the rotation of a vector in $\mathbb{R}^2$ by an angle $\alpha$ vividly illustrates this:
$$ \begin{pmatrix} \cos \alpha & -\sin \alpha \\ \sin \alpha & \cos \alpha \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = \begin{pmatrix} x_1 \cos \alpha - x_2 \sin \alpha \\ x_1 \sin \alpha + x_2 \cos \alpha \end{pmatrix} $$
For instance, rotating a vector by $\alpha = \pi/4$:
$$ \begin{pmatrix} \frac{\sqrt{2}}{2} & -\frac{\sqrt{2}}{2} \\ \frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2} \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = \frac{\sqrt{2}}{2} \begin{pmatrix} x_1 - x_2 \\ x_1 + x_2 \end{pmatrix} $$
Finally, the lecture connected this matrix-vector multiplication to solving [systém lineárních rovnic](https://felwiki.basta.one/en/Concepts/syst-m-line-rn-ch-rovnic-system-of-linear-equations_mc_systém-lineárních-rovnic-system-of-linear-equations). The equation $A \cdot x = b$ can be interpreted in two ways:
1.  Finding the [vzor](https://felwiki.basta.one/en/Concepts/vzor-preimage_mc_vzor-preimage) of point $b$ under the linear transformation $A: F^s \to F^r$.
2.  Solving a [systém lineárních rovnic](https://felwiki.basta.one/en/Concepts/syst-m-line-rn-ch-rovnic-system-of-linear-equations_mc_systém-lineárních-rovnic-system-of-linear-equations), where the number of columns of $A$ is the number of unknowns, and the number of rows is the number of equations.

The lecture concluded by previewing the topic of matrix multiplication, which will be the focus of the next lecture (Topic 4B), explaining that the composition of linear transformations (e.g., $P_x \circ R_\alpha$) corresponds to a new matrix, and the method for finding this new matrix will be explored in the subsequent session.

### Keywords
Linear Transformations, Matrices, Vector Spaces, Geometric Transformations, Linear Algebra