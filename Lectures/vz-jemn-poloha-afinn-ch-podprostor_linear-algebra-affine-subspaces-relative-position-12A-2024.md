# Vzájemná poloha afinních podprostorů

## Lineární algebra - 12A-2024

**Lecturer:** Jiří Velebil

This lecture, "Vzájemná poloha afinních podprostorů" (Relative Position of Affine Subspaces), provides a comprehensive exploration of [affine subspaces](https://felwiki.basta.one/en/Concepts/afinn-podprostor-affine-subspace_mc_afinní-podprostor-affine-subspace.md) in linear algebra. It defines what constitutes an affine subspace, discusses various ways to represent them, and, most importantly, establishes criteria for classifying their relative positions in higher-dimensional spaces. The lecture draws upon concepts from the theory of linear equation systems and prepares students for more advanced topics involving distances and vector products.

### Understanding Affine Subspaces

The lecture began by revisiting familiar ground: the general solution to a system of linear equations $Ax = b$. As we already know, this solution takes the form $p + \text{ker}(A)$, where $p$ is a particular solution and $\text{ker}(A)$ is the kernel (null space) of matrix $A$. This set $p + \text{ker}(A)$ is a $d$-dimensional [affine subspace](https://felwiki.basta.one/en/Concepts/afinn-podprostor-affine-subspace_mc_afinní-podprostor-affine-subspace.md) in the space $F^S$, passing through the point $p$.

Formally, an [affine subspace](https://felwiki.basta.one/en/Concepts/afinn-podprostor-affine-subspace_mc_afinní-podprostor-affine-subspace.md) of $R^n$ is defined as any set of the form $p + W = \{p + x \mid x \in W\}$, where $W$ is a linear subspace of $R^n$ and $p$ is a point in $R^n$. The linear subspace $W$ is critically important and is termed the [direction of the affine subspace](https://felwiki.basta.one/en/Concepts/sm-r-afinn-ho-podprostoru-direction-of-an-affine-subspace_mc_směr-afinního-podprostoru-direction-of-an-affine-subspace.md) $p + W$. The [dimension of the affine space](https://felwiki.basta.one/en/Concepts/dimense-afinn-ho-prostoru-dimension-of-an-affine-space_mc_dimense-afinního-prostoru-dimension-of-an-affine-space.md) $p + W$ is simply the dimension of its direction, $\text{dim}(W)$. For instance, in $R^n$, 0-dimensional affine subspaces are points, 1-dimensional are lines, and 2-dimensional are planes.

### Classifying Relative Positions

A central theme of the lecture is the classification of the [relative position](https://felwiki.basta.one/en/Concepts/r-znob-n-afinn-podprostory-intersecting-affine-subspaces_mc_různoběžné-afinní-podprostory-intersecting-affine-subspaces.md) of two affine subspaces, $\pi = p + W$ and $\pi' = p' + W'$. Three main categories are defined:

1.  **[Parallel Affine Subspaces](https://felwiki.basta.one/en/Concepts/rovnob-n-afinn-podprostory-parallel-affine-subspaces_mc_rovnoběžné-afinní-podprostory-parallel-affine-subspaces.md):** $\pi$ and $\pi'$ are parallel if one direction subspace is contained within the other, i.e., $W \subseteq W'$ or $W' \subseteq W$. The [degree of parallelism](https://felwiki.basta.one/en/Concepts/stupe-rovnob-nosti-degree-of-parallelism_mc_stupeň-rovnoběžnosti-degree-of-parallelism.md) is given by $\text{dim}(W \cap W')$.
2.  **[Intersecting Affine Subspaces](https://felwiki.basta.one/en/Concepts/r-znob-n-afinn-podprostory-intersecting-affine-subspaces_mc_různoběžné-afinní-podprostory-intersecting-affine-subspaces.md):** If they are not parallel and share at least one common point, they are intersecting.
3.  **[Skew Affine Subspaces](https://felwiki.basta.one/en/Concepts/mimob-n-afinn-podprostory-skew-affine-subspaces_mc_mimoběžné-afinní-podprostory-skew-affine-subspaces.md):** If they are not parallel and have no common points, they are skew.

To systematically determine the relative position, a logical flowchart is recommended: first check for parallelism, and if not parallel, then check for intersection.

### Characterization Theorems

The lecture provided rigorous characterizations for these relative positions.
For **parallel and disjoint** affine subspaces $\pi = p + W$ and $\pi' = p' + W'$ (assuming $W' \subseteq W$), the following conditions are equivalent:
*   $\pi$ and $\pi'$ are disjoint.
*   The vector $p - p'$ does not lie in $W$.
These conditions highlight that if they are parallel, their disjointness depends solely on whether the vector connecting their reference points is contained within the larger direction subspace.

For **intersecting** affine subspaces $\pi = p + W$ and $\pi' = p' + W'$ that are not parallel, the following are equivalent:
*   $\pi$ and $\pi'$ are intersecting.
*   The vector $p - p'$ lies in $W \vee W'$, where $W \vee W'$ denotes the join (sum) of the subspaces $W$ and $W'$.

For **skew** affine subspaces $\pi = p + W$ and $\pi' = p' + W'$ that are not parallel, the following are equivalent:
*   $\pi$ and $\pi'$ are skew.
*   The vector $p - p'$ does not lie in $W \vee W'$.

### Representations of Affine Subspaces

Affine subspaces can be described in two primary ways:

1.  **[Parametric Representation](https://felwiki.basta.one/en/Concepts/parametrick-z-pis-parametric-representation_mc_parametrický-zápis-parametric-representation.md):** For a $d$-dimensional affine subspace $\pi = p + W$, there exists a matrix $S: R^d \to R^n$ such that $x \in \pi$ if and only if $x = p + S \cdot t$ for some $t \in R^d$. Here, $\text{im}(S) = W$ and $\text{rank}(S) = d$. This form explicitly shows a starting point $p$ and directions spanned by the columns of $S$.
    *   Formula: $x = p + S \cdot t$
    *   Description: Parametric representation of an affine subspace, where $S$ is a matrix spanning the direction subspace $W$ and $t$ is a parameter vector.

2.  **[Equation Representation](https://felwiki.basta.one/en/Concepts/rovnicov-z-pis-equation-representation_mc_rovnicový-zápis-equation-representation.md):** An affine subspace $\pi = p + W$ can also be described by an equation $N^T \cdot (x - p) = o$, where $N^T: R^n \to R^{n-d}$ is a matrix such that $\text{ker}(N^T) = W$ and $\text{rank}(N) = n-d$. The columns of $N$ represent "normal" vectors orthogonal to the subspace's direction. The point $p$ naturally satisfies the equation $N^T \cdot (p - p) = o$, confirming that the affine subspace passes through $p$.
    *   Formula: $N^T \cdot (x - p) = o$
    *   Description: Equation representation of an affine subspace, where $N$ is a matrix of normal vectors and $o$ is the zero vector.

The equivalence of these representations is crucial for practical calculations. For instance, determining parallelism or intersection often boils down to checking the solvability of systems of linear equations involving the direction vectors (columns of $S$ and $S'$) and the difference vector $p - p'$.

### Practical Examples of Relative Position

The lecture extensively used examples to illustrate the process of determining relative positions, emphasizing a step-by-step approach consistent with the conceptual flowchart. These examples involved applying the characterization theorems by setting up and solving appropriate linear systems, often leveraging [Gaussian elimination](https://felwiki.basta.one/en/Concepts/gaussova-eliminace-gaussian-elimination_mc_gaussova-eliminace-gaussian-elimination.md).

For instance, two planes in $R^5$, $\pi = [0, 0, 0, 0, 1]^T + \text{span}([1, 0, 0, 0, 0]^T, [0, 1, 0, 0, 0]^T)$ and $\pi' = [0, 0, 0, 1, 0]^T + \text{span}([1, 0, 0, 0, 0]^T, [0, 1, 0, 0, 0]^T)$, were analyzed. First, their parallelism was checked by verifying if their direction subspaces (spanned by $S$ and $S'$) were subsets of each other. Since this was not the case, they were deemed not parallel. Next, their intersection was checked by solving a system with the augmented matrix $(S' | S | p - p')$. The lack of a solution indicated that they are [skew affine subspaces](https://felwiki.basta.one/en/Concepts/mimob-n-afinn-podprostory-skew-affine-subspaces_mc_mimoběžné-afinní-podprostory-skew-affine-subspaces.md).

Similarly, various examples of lines in $R^3$ and planes in $R^4$ were discussed, demonstrating how to:
*   Identify parallel and disjoint lines (same direction, no common point).
*   Identify intersecting lines (different directions, common point).
*   Identify skew lines (different directions, no common point).

The common thread in all these examples is the systematic application of the definitions and theorems, reducing the geometric problem to an algebraic one of solving linear systems.

### Concluding Remarks and Future Topics

The concepts of parallelism, intersection, and skewness, along with the existence of parametric and equation representations, are generalizable beyond $R^n$ to any space $F^n$ over an arbitrary field $F$. This highlights the broad applicability of these linear algebra principles.

Looking ahead, future lectures will build upon these foundations by introducing the [vector product](https://felwiki.basta.one/en/Concepts/vektorov-sou-in_mc_vektorový-součin.md) in $R^n$ (for $n \geq 2$) and teaching how to calculate the [mutual distance of affine subspaces](https://felwiki.basta.one/en/Concepts/vz-jemn-vzd-lenost-afinn-ch-podprostor_mc_vzájemná-vzdálenost-afinních-podprostorů.md) in $R^n$. These future topics will significantly utilize the properties of the [standard scalar product](https://felwiki.basta.one/en/Concepts/standardn-skal-rn-sou-in_mc_standardní-skalární-součin.md) in $R^n$.

### Keywords
linear algebra, affine subspaces, vector spaces, relative position, parametric equations, equation form, linear systems