# Metrické výpočty v Rⁿ

## Lineární algebra - 13A-2024

This lecture was presented by Jiří Velebil.

This lecture provided a comprehensive exploration of defining and calculating the mutual distance between two affine subspaces in Rⁿ, with a particular focus on practical applications in R² and R³. It revisited fundamental concepts of linear algebra and geometry, establishing the theoretical framework before delving into specific computational methods.

The session began by reviewing foundational concepts essential for understanding metric calculations in vector spaces. Key among these are the [Standard scalar product](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in_mc_standardní-skalární-součin) in Rⁿ, defined as $\langle \mathbf{x} \mid \mathbf{y} \rangle = \mathbf{x}^T \cdot \mathbf{y}$. Building upon this, the [Norm](https://felwiki.basta.one/en/Concepts/norma_mc_norma) of a vector $\mathbf{x}$ was introduced as $||\mathbf{x}|| = \sqrt{\langle \mathbf{x} \mid \mathbf{x} \rangle} = \sqrt{\mathbf{x}^T \cdot \mathbf{x}}$. These definitions naturally lead to the [Euclidean distance](https://felwiki.basta.one/en/Concepts/eukleidovsk-vzd-lenost_mc_eukleidovská-vzdálenost) between two vectors $\mathbf{x}$ and $\mathbf{y}$, given by $||\mathbf{x} - \mathbf{y}|| = \sqrt{\sum_{i=1}^n (x_i - y_i)^2}$.

A central concept for the lecture's topic is an [Affine subspace](https://felwiki.basta.one/en/Concepts/afinn-podprostor_mc_afinní-podprostor), defined as a set of points of the form $p + W = \{p + x \mid x \in W\}$, where $W$ is a linear subspace and $p$ is a vector. Understanding these fundamental building blocks is crucial for grasping the subsequent discussions on distances.

### Defining and Calculating Mutual Distance Between Affine Subspaces

The core objective of the lecture was to define and calculate the [Mutual distance of affine subspaces](https://felwiki.basta.one/en/Concepts/vz-jemn-vzd-lenost-afinn-ch-podprostor_mc_vzájemná-vzdálenost-afinních-podprostorů). For two affine subspaces $\pi$ and $\pi'$ in Rⁿ, their mutual distance, denoted $\omega(\pi, \pi')$, is formally defined as the infimum of the distances between any two points from each subspace:
$$
\omega(\pi, \pi') = \inf\{\|\mathbf{x} - \mathbf{x}'\| \mid \mathbf{x} \in \pi, \mathbf{x}' \in \pi'\}
$$
This definition ensures that the distance is the shortest possible separation between any two points belonging to the respective subspaces.

A key theorem presented in the lecture provides a general formula for calculating this mutual distance. If $\pi = \mathbf{p} + W$ and $\pi' = \mathbf{p}' + W'$ are two affine subspaces, their mutual distance is given by:
$$
\omega(\pi, \pi') = \|\operatorname{rej}_{W \vee W'}(\mathbf{p} - \mathbf{p}')\|
$$
Here, $W \vee W'$ represents the sum of the linear subspaces $W$ and $W'$, and $\operatorname{rej}$ denotes the [Orthogonal rejection](https://felwiki.basta.one/en/Concepts/ortogon-ln-rejekce_mc_ortogonální-rejekce). The proof of this formula relies heavily on the properties of orthogonal rejection and the [Pythagorean theorem](https://felwiki.basta.one/en/Concepts/pythagorova-v-ta_mc_pythagorova-věta). Specifically, the [Orthogonal projection](https://felwiki.basta.one/en/Concepts/ortogon-ln-projekce_mc_ortogonální-projekce) of a vector $\mathbf{x}$ onto the span of a vector $\mathbf{v}$ is given by $\operatorname{proj}_{\operatorname{span}(\mathbf{v})}(\mathbf{x}) = \frac{\langle \mathbf{v} \mid \mathbf{x} \rangle}{\langle \mathbf{v} \mid \mathbf{v} \rangle} \cdot \mathbf{v}$, and the orthogonal rejection is defined as $\operatorname{rej}_{\operatorname{span}(\mathbf{v})}(\mathbf{x}) = \mathbf{x} - \operatorname{proj}_{\operatorname{span}(\mathbf{v})}(\mathbf{x})$. This theorem provides a powerful tool for calculating distances in various geometric settings.

### Practical Applications in R² and R³

The lecture then applied this general framework to derive specific formulas for calculating distances in lower-dimensional spaces, R² and R³.

#### Distance Calculations in R²

For two-dimensional space, the lecture covered:

*   **Distance of a Point from a Line:** The distance from a point $\mathbf{p}'$ to a line $\pi$ defined by $\mathbf{n}^T(\mathbf{x}-\mathbf{p})=0$ (where $\mathbf{n}$ is the normal vector) is given by:
    $$
    \omega(\mathbf{p}', \pi) = \frac{\left|\mathbf{n}^T(\mathbf{p}' - \mathbf{p})\right|}{\|\mathbf{n}\|}
    $$
    This formula is particularly useful when the line is given in its implicit form.

*   **Distance of Two Lines:** The distance between two lines in R² depends on their relationship. If the lines are [intersecting affine subspaces](https://felwiki.basta.one/en/Concepts/r-znob-n-afinn-podprostory-intersecting-affine-subspaces_mc_různoběžné-afinní-podprostory-intersecting-affine-subspaces), their mutual distance is zero. If they are [parallel affine subspaces](https://felwiki.basta.one/en/Concepts/rovnob-n-afinn-podprostory-parallel-affine-subspaces_mc_rovnoběžné-afinní-podprostory-parallel-affine-subspaces), the distance can be calculated as the distance from any point on one line to the other line, using the point-line distance formula.

#### Distance Calculations in R³

In three-dimensional space, calculations become more complex due to the possibility of skew lines and planes.

*   **Distance of a Point from a Line:** Similar to R², the distance from a point to a line in R³ can be found using the general orthogonal rejection formula or by finding the length of the vector from the point to its projection on the line.

*   **Distance of a Point from a Plane:** For a point $\mathbf{p}'$ and a plane $\pi$ defined by $\mathbf{n}^T(\mathbf{x}-\mathbf{p})=0$, the distance is identical in form to the point-line distance in R²:
    $$
    \omega(\mathbf{p}', \pi) = \frac{\left|\mathbf{n}^T(\mathbf{p}' - \mathbf{p})\right|}{\|\mathbf{n}\|}
    $$
    Here, the normal vector $\mathbf{n}$ for a plane defined by $\mathbf{p} + \operatorname{span}(\mathbf{s}_1, \mathbf{s}_2)$ can be found using the [Vector product](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin) as $\mathbf{n} = \mathbf{s}_1 \times \mathbf{s}_2$.

*   **Distance of a Line from a Plane:**
    *   If a line is not parallel to a plane, they must intersect, and their distance is zero.
    *   If a line $\pi'$ (defined by $\mathbf{p}' + \operatorname{span}(\mathbf{s}')$) is parallel to a plane $\pi$ (defined by $\mathbf{p} + \operatorname{span}(\mathbf{s}_1, \mathbf{s}_2)$), their distance is given by:
        $$
        \omega(\pi', \pi) = \frac{\left|\det(\mathbf{s}_1, \mathbf{s}_2, \mathbf{p}' - \mathbf{p})\right|}{\sqrt{\operatorname{Gram}(\mathbf{s}_1, \mathbf{s}_2)}}
        $$
        This formula involves the determinant of a matrix formed by direction vectors and the difference between points, normalized by the square root of the [Gram determinant](https://felwiki.basta.one/en/Concepts/gram-v-determinant_mc_gramův-determinant) of the plane's spanning vectors.

*   **Distance of Two Lines in R³:**
    *   If two lines are [intersecting affine subspaces](https://felwiki.basta.one/en/Concepts/r-znob-n-afinn-podprostory-intersecting-affine-subspaces_mc_různoběžné-afinní-podprostory-intersecting-affine-subspaces) or [parallel affine subspaces](https://felwiki.basta.one/en/Concepts/rovnob-n-afinn-podprostory-parallel-affine-subspaces_mc_rovnoběžné-afinní-podprostory-parallel-affine-subspaces), the calculation simplifies (zero distance for intersecting, point-line distance for parallel).
    *   For [skew affine subspaces](https://felwiki.basta.one/en/Concepts/mimob-n-afinn-podprostory-skew-affine-subspaces_mc_mimoběžné-afinní-podprostory-skew-affine-subspaces) $\pi'$ (defined by $\mathbf{p}' + \operatorname{span}(\mathbf{s}')$) and $\pi$ (defined by $\mathbf{p} + \operatorname{span}(\mathbf{s})$), the distance is:
        $$
        \omega(\pi', \pi) = \frac{\left|\det(\mathbf{s}', \mathbf{s}, \mathbf{p}' - \mathbf{p})\right|}{\sqrt{\operatorname{Gram}(\mathbf{s}', \mathbf{s})}}
        $$
        This formula, similar to the line-plane case, uses the determinant involving the direction vectors of both lines and the difference between their reference points, normalized by the Gram determinant of the direction vectors.

### Conclusion

In summary, this lecture provided a thorough foundation for understanding and calculating metric properties in Rⁿ, particularly the [Mutual distance of affine subspaces](https://felwiki.basta.one/en/Concepts/vz-jemn-vzd-lenost-afinn-ch-podprostor_mc_vzájemná-vzdálenost-afinních-podprostorů). The key takeaway is the general formula $\omega(\pi, \pi') = \|\operatorname{rej}_{W \vee W'}(\mathbf{p} - \mathbf{p}')\|$, which leverages the concepts of [Orthogonal projection](https://felwiki.basta.one/en/Concepts/ortogon-ln-projekce_mc_ortogonální-projekce) and [Orthogonal rejection](https://felwiki.basta.one/en/Concepts/ortogon-ln-rejekce_mc_ortogonální-rejekce). Students should be able to apply this general principle creatively to solve specific distance problems in R² and R³, understanding when to use simplified formulas involving normal vectors or determinants and Gram matrices, depending on the geometric configuration of the subspaces.

### Keywords
Linear Algebra, Metric Spaces, Affine Subspaces, Distance Calculation, Euclidean Geometry