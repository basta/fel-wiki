# Abstraktní skalární součin

## Lineární algebra - 09B-2024
**Speaker:** Jiří Velebil

This lecture provided a comprehensive introduction to the concept of an [Abstraktní skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in-scalar-product) within general linear spaces, significantly expanding upon the familiar geometric notions derived from $\mathbb{R}^n$. The primary objective was to establish an axiomatic definition of the scalar product, allowing the elegant transfer of concepts like orthogonality, vector length, and angles into abstract vector spaces. While primarily focusing on linear spaces over real numbers ($\mathbb{R}$), the lecture briefly acknowledged linear spaces over complex numbers ($\mathbb{C}$) due to their relevance in physics and quantum computing. Fundamentally, a scalar product serves as a measure of the "deviation" or "alignment" between two vectors.

### Defining the Abstract Scalar Product

The lecture began by defining a real [skalární součin](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in) axiomatically for a linear space $L$ over $\mathbb{R}$ as a function $\langle - | - \rangle : L \times L \rightarrow \mathbb{R}$. This function must satisfy three crucial properties for any vectors $\vec{x}, \vec{y}, \vec{z} \in L$ and scalar $a \in \mathbb{R}$:

1.  **Commutativity:** $\langle \vec{x} | \vec{y} \rangle = \langle \vec{y} | \vec{x} \rangle$.
2.  **Linearity in the second coordinate:** The mapping $\vec{y} \mapsto \langle \vec{x} | \vec{y} \rangle$ is linear, meaning $\langle \vec{x} | \vec{y} + \vec{z} \rangle = \langle \vec{x} | \vec{y} \rangle + \langle \vec{x} | \vec{z} \rangle$ and $\langle \vec{x} | a\vec{y} \rangle = a \langle \vec{x} | \vec{y} \rangle$.
3.  **[Positivní definitnost](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice_mc_positivně-definitní-matice.md):** $\langle \vec{x} | \vec{x} \rangle \ge 0$, and $\langle \vec{x} | \vec{x} \rangle = 0$ if and only if $\vec{x} = \vec{0}$.

For complex linear spaces, the commutativity property is replaced by conjugate symmetry: $\langle \vec{x} | \vec{y} \rangle = \overline{\langle \vec{y} | \vec{x} \rangle}$. The lecture adopted the Dirac bra-ket notation ($\langle \cdot | \cdot \rangle$) for scalar products, noting its advantages over dot notation ($\vec{x} \cdot \vec{y}$).

### Examples and Derived Concepts

Several examples illustrated the versatility of scalar products:
*   The geometric scalar product in the space of oriented line segments: $\langle \vec{x} | \vec{y} \rangle = ||\vec{x}|| \cdot ||\vec{y}|| \cos\varphi$, where $\varphi$ is the angle between vectors. This foundational example serves as a blueprint for how geometric intuition translates into abstract spaces.
*   The [Standardní skalární součin v $\mathbb{R}^n$](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in_mc_standardní-skalární-součin.md): For vectors $\vec{x} = (x_1, \dots, x_n)$ and $\vec{y} = (y_1, \dots, y_n)$, it's defined as $\langle \vec{x} | \vec{y} \rangle = \sum_{i=1}^n x_i y_i$.
*   An example of a non-standard scalar product in $\mathbb{R}^2$: $\langle (x_1, x_2) | (y_1, y_2) \rangle = x_1 y_1 + x_2 y_1 + x_1 y_2 + 2x_2 y_2$. This demonstrates that the standard scalar product is not unique.
*   The standard scalar product in $\mathbb{C}^n$: $\langle \vec{x} | \vec{y} \rangle = \sum_{i=1}^n x_i \overline{y_i}$, where $\overline{y_i}$ denotes the complex conjugate.

A critical concept derived from the scalar product is the [norma](https://felwiki.basta.one/en/Concepts/norma_mc_norma.md) (or length) of a vector, defined as $||\vec{x}|| = \sqrt{\langle \vec{x} | \vec{x} \rangle}$. This norm satisfies key properties: non-negativity ($||\vec{x}|| \ge 0$, and $||\vec{x}|| = 0$ iff $\vec{x} = \vec{0}$), scalar homogeneity ($||a\vec{x}|| = |a| \cdot ||\vec{x}||$), and the vital Triangle Inequality: $||\vec{x} + \vec{y}|| \le ||\vec{x}|| + ||\vec{y}||$.

### The Cauchy-Schwarz-Bunyakovsky Inequality

A cornerstone of scalar product theory is the [Cauchy-Schwarz](https://felwiki.basta.one/en/Concepts/cauchy-schwarz) Inequality:
$$|\langle \vec{x} | \vec{y} \rangle| \le \sqrt{\langle \vec{x} | \vec{x} \rangle} \cdot \sqrt{\langle \vec{y} | \vec{y} \rangle}$$
This can also be written concisely in terms of norms as $|\langle \vec{x} | \vec{y} \rangle| \le ||\vec{x}|| \cdot ||\vec{y}||$. This inequality is fundamental, as it ensures that the definition of an angle between two non-zero vectors, $\cos\varphi = \frac{\langle \vec{x} | \vec{y} \rangle}{||\vec{x}|| \cdot ||\vec{y}||}$, results in a cosine value between -1 and 1, allowing for a unique angle $\varphi \in [0, \pi]$.

### Orthogonality and Geometric Theorems

The lecture defined [ortogonální vektory](https://felwiki.basta.one/en/Concepts/ortogon-ln-vektory_mc_ortogonální-vektory.md) (or mutually perpendicular vectors) as two vectors $\vec{x}$ and $\vec{y}$ for which their scalar product $\langle \vec{x} | \vec{y} \rangle = 0$. Notably, the zero vector $\vec{0}$ is orthogonal to every vector, and conversely, if a vector is orthogonal to all other vectors, it must be the zero vector itself. An important practical takeaway is that to verify orthogonality between a vector $\vec{x}$ and a subspace spanned by a set of vectors $M$, it suffices to check that $\vec{x}$ is orthogonal to all vectors in $M$. This highlights that "orthogonality only needs to be verified for a set of generators of a subspace."

The geometric significance of the abstract scalar product was further demonstrated through generalisations of classical theorems:
*   **Cosine Rule:** For non-zero vectors $\vec{x}$ and $\vec{y}$ forming a triangle, $||\vec{x} - \vec{y}||^2 = ||\vec{x}||^2 + ||\vec{y}||^2 - 2\langle \vec{x} | \vec{y} \rangle$.
*   **[Pythagorova věta](https://felwiki.basta.one/en/Concepts/pythagorova-v-ta_mc_pythagorova-věta.md):** A special case of the Cosine Rule, stating that if $\langle \vec{x} | \vec{y} \rangle = 0$, then $||\vec{x} - \vec{y}||^2 = ||\vec{x}||^2 + ||\vec{y}||^2$.
*   **Parallelogram Identity:** For any two vectors $\vec{x}$ and $\vec{y}$, $||\vec{x} - \vec{y}||^2 + ||\vec{x} + \vec{y}||^2 = 2(||\vec{x}||^2 + ||\vec{y}||^2)$.

These theorems confirm that the geometric intuition from classical Euclidean space extends seamlessly into general linear spaces equipped with a scalar product.

### Scalar Products, Norms, and Metrics

The lecture explained the hierarchical relationship: a scalar product induces a norm, and that norm, in turn, induces a metric (or distance function) on the linear space $L$. The metric $d(\vec{x}, \vec{y})$ is defined as $d(\vec{x}, \vec{y}) = ||\vec{x} - \vec{y}||$. This metric satisfies standard properties: non-negativity, symmetry, and the triangle inequality. However, the inverse implications do not hold: not every norm is induced by a scalar product (e.g., the sum of absolute values norm in $\mathbb{R}^2$ doesn't satisfy the parallelogram identity), and not every metric is induced by a norm.

### Beyond Positive Definiteness: The Lorentz Metric

The discussion also veered into areas where the [positivně definitní matice (positive definite matrix)](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice-positive-definite-matrix_mc_positivně-definitní-matice-positive-definite-matrix.md) condition is relaxed. A notable example is the "[Lorentzova metrika (Lorentz Metric)](https://felwiki.basta.one/en/Concepts/lorentzova-metrika-lorentz-metric_mc_lorentzova-metrika-lorentz-metric.md)" in $\mathbb{R}^4$, used in the theory of relativity for Minkowski spacetime. Defined as $\langle (t,x,y,z) | (t',x',y',z') \rangle = tt' - xx' - yy' - zz'$, this is not positive definite (e.g., $\langle (0,1,0,0) | (0,1,0,0) \rangle = -1$). This non-positive definite "scalar product" allows for concepts like time dilation and length contraction, where Lorentz transformations can be interpreted as hyperbolic rotations.

### Matrix Representation of Scalar Products

Finally, the lecture touched upon how scalar products in $\mathbb{R}^n$ can be represented by matrices. For the [Standardní skalární součin v $\mathbb{R}^n$](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in_mc_standardní-skalární-součin.md), applying a linear transformation (matrix $A$) preserves the scalar product if and only if $A^T A = E_n$ (where $E_n$ is the identity matrix), meaning $A$ is an [orthogonal matrix](https://felwiki.basta.one/en/Concepts/orthogonal-matrix_mc_orthogonal-matrix.md). Examples like [rotace (rotation)](https://felwiki.basta.one/en/Concepts/rotace-rotation_mc_rotace-rotation.md) and reflections preserve the standard scalar product, while projections and scaling do not. For an arbitrary scalar product in $\mathbb{R}^n$, it can be expressed using a matrix $G$ such that $\langle \vec{x} | \vec{y} \rangle = \vec{x}^T G \vec{y}$. The lecture concluded by posing the question of which matrices $G$ define scalar products in $\mathbb{R}^n$, foreshadowing the concept of [positivně definitní matice (positive definite matrix)](https://felwiki.basta.one/en/Concepts/positivn-definitn-matice-positive-definite-matrix_mc_positivně-definitní-matice-positive-definite-matrix.md) as the answer for the next lecture.

**Keywords:** skalární součin, lineární algebra, vektory, ortogonalita, Cauchy-Schwarz