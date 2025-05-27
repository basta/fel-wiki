# Ortogonalisace a ortogonální projekce

## Lineární algebra - 10B-2024
**Speaker:** Jiří Velebil

This lecture provides a comprehensive introduction to orthogonal sets, orthogonal and orthonormal bases, and the critical concept of orthogonal projection within linear spaces. The focus is exclusively on linear spaces over the field of real numbers ($\mathbb{R}$). The lecture delves into the theoretical underpinnings, practical computational advantages of orthonormal bases, and details the iterative Gram-Schmidt orthogonalization process, which is fundamental for transforming any given basis into an orthogonal, and subsequently orthonormal, one. It also highlights the significance of orthogonal rejection, especially its "shortest distance" property, which forms the basis for important applications like the [Method of Least Squares](https://felwiki.basta.one/en/Concepts/metoda-nejmen-ch-tverc-least-squares-method_mc_metoda-nejmenších-čtverců-least-squares-method.md).

### Fundamentals of Orthogonality

The lecture began by recalling the basic definition of [Orthogonal Vectors](https://felwiki.basta.one/en/Concepts/orthogonal-vectors_mc_orthogonal-vectors.md). Two vectors $\vec{x}$ and $\vec{y}$ are considered orthogonal (or mutually perpendicular) if their [Scalar Product](https://felwiki.basta.one/en/Concepts/skal-rn-sou-in-scalar-product_mc_skalární-součin-scalar-product.md) $(\vec{x} | \vec{y})$ is zero. A crucial property noted is that the zero vector $\vec{0}$ is orthogonal to every vector. Conversely, if a vector is orthogonal to every other vector, it must be the zero vector itself.

The discussion extended to sets of vectors. An [Orthogonal Set](https://felwiki.basta.one/en/Concepts/orthogonal-set_mc_orthoal-set.md) is defined as any set of non-zero vectors where all distinct pairs of vectors are orthogonal. A significant theorem asserts that such an orthogonal set of non-zero vectors is always [Linearly Independent](https://felwiki.basta.one/en/Concepts/line-rn-nez-vislost_mc_lineární-nezávislost.md). This implies that in an $n$-dimensional space, there can be at most $n$ mutually orthogonal non-zero vectors.

### Orthogonal and Orthonormal Bases

Building upon the concept of orthogonal sets, the lecture defined an [Orthogonal Basis](https://felwiki.basta.one/en/Concepts/orthogonal-basis_mc_orthogonal-basis.md) as an orthogonal set that also forms a basis for the linear space. This can be conceptualized as a "right-angled coordinate system." Further, an [Orthonormal Basis](https://felwiki.basta.one/en/Concepts/ortonorm-ln-b-ze_mc_ortonormální-báze.md) is introduced as an orthogonal basis where all basis vectors have a [Norm](https://felwiki.basta.one/en/Concepts/norma_mc_norma.md) of 1. This condition is formally expressed using the [Kronecker Delta](https://felwiki.basta.one/en/Concepts/kronecker-delta_mc_kronecker-delta.md) symbol $\delta_{ij}$, such that $(\vec{b}_i | \vec{b}_j) = \delta_{ij}$. The canonical basis in $\mathbb{R}^n$ with the standard scalar product serves as a prime example of an orthonormal basis.

Orthonormal bases are particularly important because they significantly simplify computations. The lecture demonstrated two key advantages:

1.  **Computation of Coordinates:** For a vector $\vec{x}$ in an orthonormal basis $B = (\vec{b}_1, \ldots, \vec{b}_n)$, its coordinates are directly given by the scalar products with the basis vectors:
    $$ \vec{x} = \sum_{i=1}^{n} (\vec{b}_i | \vec{x}) \cdot \vec{b}_i $$
    This means $\text{coord}_B(\vec{x}) = ((\vec{b}_1|\vec{x}), \ldots, (\vec{b}_n|\vec{x}))^T$.

2.  **Computation of Scalar Product:** The scalar product of two vectors $\vec{x}$ and $\vec{y}$ in an orthonormal basis $B$ can be computed simply as the standard scalar product of their coordinate vectors:
    $$ (\vec{x} | \vec{y}) = \sum_{i=1}^{n} (\vec{b}_i | \vec{x}) \cdot (\vec{b}_i | \vec{y}) $$
    This is equivalent to $\vec{x}^T \vec{y}$ where $\vec{x}$ and $\vec{y}$ are the coordinate vectors.

Furthermore, the lecture showed how to determine the angles a vector $\vec{x}$ makes with the coordinate axes in an orthonormal basis. For the angle $\varphi_{i_0}$ between $\vec{x}$ and a basis vector $\vec{b}_{i_0}$:
$$ \cos \varphi_{i_0} = \frac{(\vec{b}_{i_0} | \vec{x})}{||\vec{x}||} $$
A notable identity related to these angles is $\sum \cos^2 \varphi_i = 1$, which generalizes the Pythagorean identity from elementary geometry.

### Orthogonal Projection and Rejection

A significant portion of the lecture focused on [Orthogonal Projection](https://felwiki.basta.one/en/Concepts/ortogon-ln-projekce-orthogonal-projection_mc_ortogonální-projekce-orthogonal-projection.md) and [Orthogonal Rejection](https://felwiki.basta.one/en/Concepts/ortogon-ln-rejekce-orthogonal-rejection_mc_ortogonální-rejekce-orthogonal-rejection.md). For any non-zero vector $\vec{s}$ and any vector $\vec{x}$, $\vec{x}$ can be uniquely decomposed into two orthogonal components:
*   **Orthogonal Projection onto a line:** The component of $\vec{x}$ that lies along the line spanned by $\vec{s}$:
    $$ \text{proj}_{\vec{s}}(\vec{x}) = \frac{(\vec{s}|\vec{x})}{(\vec{s}|\vec{s})} \cdot \vec{s} $$
*   **Orthogonal Rejection from a line:** The component of $\vec{x}$ that is orthogonal to the line spanned by $\vec{s}$:
    $$ \text{rej}_{\vec{s}}(\vec{x}) = \vec{x} - \frac{(\vec{s}|\vec{x})}{(\vec{s}|\vec{s})} \cdot \vec{s} $$
This concept was then generalized to projection and rejection onto/from a subspace $W$. The [Orthogonal Projection](https://felwiki.basta.one/en/Concepts/ortogon-ln-projekce-orthogonal-projection_mc_ortogonální-projekce-orthogonal-projection.md) $\text{proj}_W(\vec{x})$ is the vector in $W$ such that $\vec{x} - \text{proj}_W(\vec{x})$ is orthogonal to all vectors in $W$. The [Orthogonal Rejection](https://felwiki.basta.one/en/Concepts/ortogon-ln-rejekce-orthogonal-rejection_mc_ortogonální-rejekce-orthogonal-rejection.md) is then $\text{rej}_W(\vec{x}) = \vec{x} - \text{proj}_W(\vec{x})$.

A crucial property of orthogonal rejection is that it represents the "shortest" distance from a vector $\vec{x}$ to the subspace $W$. This is demonstrated by the [Pythagorean Theorem](https://felwiki.basta.one/en/Concepts/pythagorova-v-ta_mc_pythagorova-věta.md): for any vector $\vec{w}$ in $W$, $||\vec{x} - \text{proj}_W(\vec{x})||^2 \le ||\vec{x} - \vec{w}||^2$. This property forms the bedrock for important applications such as the [Method of Least Squares](https://felwiki.basta.one/en/Concepts/metoda-nejmen-ch-tverc-least-squares-method_mc_metoda-nejmenších-čtverců-least-squares-method.md).

For a subspace $W$ with a known orthogonal basis $M = \{\vec{u}_1, \ldots, \vec{u}_k\}$, the orthogonal projection of a vector $\vec{x}$ onto $W$ can be computed using the formula:
$$ \text{proj}_W(\vec{x}) = \sum_{i=1}^{k} \frac{(\vec{u}_i|\vec{x})}{(\vec{u}_i|\vec{u}_i)} \cdot \vec{u}_i $$

### Gram-Schmidt Orthogonalization Process

The lecture culminated in the detailed explanation of the [Gram-Schmidt Orthogonalization Process](https://felwiki.basta.one/en/Concepts/gram-schmidt-orthogonalization-process_mc_gram-schmidt-orthogonalization-process.md). This fundamental algorithm enables the transformation of any basis $B = (\vec{b}_1, \ldots, \vec{b}_n)$ of a space with a scalar product into an orthogonal basis $C = (\vec{c}_1, \ldots, \vec{c}_n)$ with two key properties:
1.  $C$ is orthogonal, meaning $(\vec{c}_i | \vec{c}_j) = 0$ for $i \ne j$.
2.  For every $k \in \{1, \ldots, n\}$, the span of the first $k$ vectors from the original basis is equal to the span of the first $k$ vectors from the new orthogonal basis: $\text{span}\{\vec{b}_1, \ldots, \vec{b}_k\} = \text{span}\{\vec{c}_1, \ldots, \vec{c}_k\}$.

The process is iterative, defining the $(k+1)$-th orthogonal vector $\vec{c}_{k+1}$ as the orthogonal rejection of $\vec{b}_{k+1}$ from the subspace spanned by the previously generated orthogonal vectors $\vec{c}_1, \ldots, \vec{c}_k$:
$$ \vec{c}_1 := \vec{b}_1 $$
$$ \vec{c}_{k+1} := \text{rej}_{\text{span}\{\vec{c}_1, \ldots, \vec{c}_k\}}(\vec{b}_{k+1}) $$
This iterative application of orthogonal rejection guarantees the desired properties.

Once an orthogonal basis $C = (\vec{c}_1, \ldots, \vec{c}_n)$ is obtained, it can be easily converted into an [Orthonormal Basis](https://felwiki.basta.one/en/Concepts/ortonorm-ln-b-ze_mc_ortonormální-báze.md) through [Normalisation](https://felwiki.basta.one/en/Concepts/normalisation_mc_normalisation.md). Each vector $\vec{c}_i$ is simply scaled by its [norm](https://felwiki.basta.one/en/Concepts/norma_mc_norma.md), resulting in the orthonormal basis $(\vec{c}_1/||\vec{c}_1||, \ldots, \vec{c}_n/||\vec{c}_n||)$.

#### Example: Gram-Schmidt Orthogonalization

The lecture provided a concrete example of the [Gram-Schmidt Orthogonalization Process](https://felwiki.basta.one/en/Concepts/gram-schmidt-orthogonalization-process_mc_gram-schmidt-orthogonalization-process.md) for a basis $B = (\vec{b}_1, \vec{b}_2, \vec{b}_3)$ of a 3-dimensional subspace in $\mathbb{R}^4$ with the standard scalar product, where $\vec{b}_1 = (1,1,1,1)^T$, $\vec{b}_2 = (0,1,1,1)^T$, and $\vec{b}_3 = (0,0,1,1)^T$.

1.  **First vector:** The first orthogonal vector $\vec{c}_1$ is simply the first original basis vector:
    $$ \vec{c}_1 = \vec{b}_1 = (1,1,1,1)^T $$

2.  **Second vector:** The second orthogonal vector $\vec{c}_2$ is obtained by rejecting $\vec{b}_2$ from the span of $\vec{c}_1$:
    $$ \text{proj}_{\text{span}\{\vec{c}_1\}}(\vec{b}_2) = \frac{(\vec{c}_1|\vec{b}_2)}{(\vec{c}_1|\vec{c}_1)} \cdot \vec{c}_1 = \frac{(1\cdot0 + 1\cdot1 + 1\cdot1 + 1\cdot1)}{(1\cdot1 + 1\cdot1 + 1\cdot1 + 1\cdot1)} \cdot (1,1,1,1)^T = \frac{3}{4} (1,1,1,1)^T $$
    $$ \vec{c}_2 = \vec{b}_2 - \text{proj}_{\text{span}\{\vec{c}_1\}}(\vec{b}_2) = (0,1,1,1)^T - \frac{3}{4}(1,1,1,1)^T = (-\frac{3}{4}, \frac{1}{4}, \frac{1}{4}, \frac{1}{4})^T $$
    To avoid fractions in subsequent calculations, $\vec{c}_2$ can be scaled by 4: $\vec{c}_2 = (-3,1,1,1)^T$. This scaling does not affect orthogonality.

3.  **Third vector:** The third orthogonal vector $\vec{c}_3$ is obtained by rejecting $\vec{b}_3$ from the span of $\vec{c}_1$ and $\vec{c}_2$:
    $$ \text{proj}_{\text{span}\{\vec{c}_1,\vec{c}_2\}}(\vec{b}_3) = \frac{(\vec{c}_1|\vec{b}_3)}{(\vec{c}_1|\vec{c}_1)} \cdot \vec{c}_1 + \frac{(\vec{c}_2|\vec{b}_3)}{(\vec{c}_2|\vec{c}_2)} \cdot \vec{c}_2 $$
    First, compute the scalar products:
    $(\vec{c}_1|\vec{b}_3) = (1\cdot0 + 1\cdot0 + 1\cdot1 + 1\cdot1) = 2$
    $(\vec{c}_1|\vec{c}_1) = 4$
    $(\vec{c}_2|\vec{b}_3) = (-3\cdot0 + 1\cdot0 + 1\cdot1 + 1\cdot1) = 2$
    $(\vec{c}_2|\vec{c}_2) = (-3)^2 + 1^2 + 1^2 + 1^2 = 9+1+1+1 = 12$
    Now substitute:
    $$ \text{proj}_{\text{span}\{\vec{c}_1,\vec{c}_2\}}(\vec{b}_3) = \frac{2}{4}(1,1,1,1)^T + \frac{2}{12}(-3,1,1,1)^T = \frac{1}{2}(1,1,1,1)^T + \frac{1}{6}(-3,1,1,1)^T $$
    $$ = (\frac{1}{2}-\frac{1}{2}, \frac{1}{2}+\frac{1}{6}, \frac{1}{2}+\frac{1}{6}, \frac{1}{2}+\frac{1}{6})^T = (0, \frac{3+1}{6}, \frac{3+1}{6}, \frac{3+1}{6})^T = (0, \frac{2}{3}, \frac{2}{3}, \frac{2}{3})^T $$
    $$ \vec{c}_3 = \vec{b}_3 - \text{proj}_{\text{span}\{\vec{c}_1,\vec{c}_2\}}(\vec{b}_3) = (0,0,1,1)^T - (0, \frac{2}{3}, \frac{2}{3}, \frac{2}{3})^T = (0, -\frac{2}{3}, \frac{1}{3}, \frac{1}{3})^T $$
    Again, scaling by 3 for simplicity: $\vec{c}_3 = (0, -2, 1, 1)^T$.

The resulting orthogonal basis is $C = (\vec{c}_1, \vec{c}_2, \vec{c}_3) = ((1,1,1,1)^T, (-3,1,1,1)^T, (0,-2,1,1)^T)$.

#### Normalization of the Orthogonal Basis

Finally, to obtain an [Orthonormal Basis](https://felwiki.basta.one/en/Concepts/ortonorm-ln-b-ze_mc_ortonormální-báze.md), each vector in the orthogonal basis $C$ is normalized by dividing it by its [norm](https://felwiki.basta.one/en/Concepts/norma_mc_norma.md):
*   $||\vec{c}_1|| = \sqrt{1^2+1^2+1^2+1^2} = \sqrt{4} = 2$. So, $\vec{c}_1/||\vec{c}_1|| = \frac{1}{2}(1,1,1,1)^T$.
*   $||\vec{c}_2|| = \sqrt{(-3)^2+1^2+1^2+1^2} = \sqrt{9+1+1+1} = \sqrt{12}$. So, $\vec{c}_2/||\vec{c}_2|| = \frac{1}{\sqrt{12}}(-3,1,1,1)^T$.
*   $||\vec{c}_3|| = \sqrt{0^2+(-2)^2+1^2+1^2} = \sqrt{0+4+1+1} = \sqrt{6}$. So, $\vec{c}_3/||\vec{c}_3|| = \frac{1}{\sqrt{6}}(0,-2,1,1)^T$.

### Conclusion

This lecture provided a thorough understanding of orthogonalization and orthogonal projection, crucial concepts in [Linear Algebra](https://felwiki.basta.one/en/Concepts/line-rn-algebra.md). It emphasized the definitions and properties of [Orthogonal Sets](https://felwiki.basta.one/en/Concepts/orthogonal-set_mc_orthogonal-set.md), [Orthogonal Bases](https://felwiki.basta.one/en/Concepts/orthogonal-basis_mc_orthogonal-basis.md), and [Orthonormal Bases](https://felwiki.basta.one/en/Concepts/ortonorm-ln-b-ze_mc_ortonormální-báze.md), highlighting their computational advantages. The detailed explanation of [Orthogonal Projection](https://felwiki.basta.one/en/Concepts/ortogon-ln-projekce-orthogonal-projection_mc_ortogonální-projekce-orthogonal-projection.md) and [Orthogonal Rejection](https://felwiki.basta.one/en/Concepts/ortogon-ln-rejekce-orthogonal-rejection_mc_ortogonální-rejekce-orthogonal-rejection.md), along with the practical demonstration of the [Gram-Schmidt Orthogonalization Process](https://felwiki.basta.one/en/Concepts/gram-schmidt-orthogonalization-process_mc_gram-schmidt-orthogonalization-process.md), equipped students with essential tools for working with vector spaces. These principles are not only fundamental to theoretical linear algebra but also form the bedrock for numerous applied mathematical techniques, notably the [Method of Least Squares](https://felwiki.basta.one/en/Concepts/metoda-nejmen-ch-tverc-least-squares-method_mc_metoda-nejmenších-čtverců-least-squares-method.md), which will be explored in future lectures.

### Keywords
Linear Algebra, Orthogonalization, Orthogonal Projection, Gram-Schmidt, Orthonormal Basis