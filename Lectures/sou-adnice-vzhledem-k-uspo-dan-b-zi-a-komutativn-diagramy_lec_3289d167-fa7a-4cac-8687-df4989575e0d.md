# Souřadnice vzhledem k uspořádané bázi a komutativní diagramy

## Lineární algebra - Jiří Velebil

This lecture, part of the Lineární algebra (Linear Algebra) course (03B-2024), delivered by Jiří Velebil, delves into two fundamental concepts: the representation of vectors using coordinates with respect to an ordered basis, and the powerful visual language of commutative diagrams. It builds upon previous discussions of bases and dimensions, providing a more concrete understanding of vector representation while simultaneously introducing abstract tools for analyzing mappings. The lecture covers topics from chapters 3.1-3.3 and 2.2 of the "Abstraktní a konkrétní lineární algebra" textbook.

### Coordinates with Respect to an Ordered Basis

The lecture began by recapping the concepts of a basis and dimension, intuitively explaining them as a selection of coordinate axes and their count, respectively. The core focus then shifted to understanding how to express a vector using these axes, leading to the definition of coordinates.

**Existence and Definition of Coordinates:**
A crucial theorem asserts that for any linear space $L$ and an [uspo-dan-b-ze-ordered-basis_mc_uspořádaná-báze-ordered-basis](https://felwiki.basta.one/en/Concepts/uspo-dan-b-ze-ordered-basis_mc_uspořádaná-báze-ordered-basis) $B = (b_1, \dots, b_n)$, every vector $x \in L$ can be uniquely expressed as a [line-rn-kombinace-linear-combination_mc_lineární-kombinace-linear-combination](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-linear-combination_mc_lineární-kombinace-linear-combination) of the basis vectors: $x = a_1 \cdot b_1 + \dots + a_n \cdot b_n$. The unique list of scalars $(a_1, \dots, a_n)$ is called the [sou-adnice-vektoru-vzhledem-k-uspo-dan-b-zi_mc_souřadnice-vektoru-vzhledem-k-uspořádané-bázi](https://felwiki.basta.one/en/Concepts/sou-adnice-vektoru-vzhledem-k-uspo-dan-b-zi_mc_souřadnice-vektoru-vzhledem-k-uspořádané-bázi) of vector $x$ with respect to the ordered basis $B$. This is commonly denoted as $\text{coord}_B(x)$, which is treated as a column vector in $F^n$:

$$ \text{coord}_{B}(\vec{x}) = \begin{pmatrix} a_1 \\ a_2 \\ \vdots \\ a_n \end{pmatrix} $$

**Illustrative Examples:**
The lecture provided examples to clarify this concept:
*   In $R^2$, with the [kanonick-b-ze-canonical-basis_mc_kanonická-báze-canonical-basis.md](https://felwiki.basta.one/en/Concepts/kanonick-b-ze-canonical-basis_mc_kanonická-báze-canonical-báze.md) $K_2 = ((1,0), (0,1))$, the coordinates of $(2,3)$ are simply $\text{coord}_{K_2}((2,3)) = (2,3)^T$. However, for a different ordered basis $B = ((2,1), (2,2))$, the same vector $(2,3)$ has different coordinates: $\text{coord}_B((2,3)) = (-1,2)^T$, because $(2,3) = -1 \cdot (2,1) + 2 \cdot (2,2)$. This highlights that coordinates are always relative to a *specific ordered basis*.
*   For the space of real polynomials of degree at most 2, $R_{\leq 2}[x]$, with ordered bases $B_1 = (1, x, x^2)$ and $B_2 = (x^2, x, 1)$, the polynomial $3x^2-2x+4$ has coordinates $\text{coord}_{B_1}(3x^2-2x+4) = (4,-2,3)^T$ and $\text{coord}_{B_2}(3x^2-2x+4) = (3,-2,4)^T$. This illustrates how the order of basis vectors directly impacts the coordinate representation.

**Linearity of Coordinate Calculation:**
A particularly important property emphasized is the [linearita-v-po-tu-sou-adnic_mc_linearita-výpočtu-souřadnic.md](https://felwiki.basta.one/en/Concepts/linearita-v-po-tu-sou-adnic_mc_linearita-výpočtu-souřadnic.md) of the coordinate mapping. For any finite ordered basis $B$ of a linear space $L$, the mapping from a vector $x$ to its coordinates $\text{coord}_B(x)$ is linear, meaning:
1.  $\text{coord}_B(x + y) = \text{coord}_B(x) + \text{coord}_B(y)$
2.  $\text{coord}_B(a \cdot x) = a \cdot \text{coord}_B(x)$
These properties are fundamental and will be further explored in the context of [line-rn-zobrazen-linear-transformation_mc_lineární-zobrazení-linear-transformation.md](https://felwiki.basta.one/en/Concepts/line-rn-zobrazen-linear-transformation_mc_lineární-zobrazení-linear-transformation.md) in future lectures.
A direct consequence of this linearity is that for any basis vector $b_i$ from $B=(b_1, \dots, b_n)$, its coordinates are a standard unit vector: $\text{coord}_B(b_1) = (1,0,\dots,0)^T$, $\text{coord}_B(b_2) = (0,1,\dots,0)^T$, and so on. More generally, for any linear combination of basis vectors, the coordinates are simply the column vector of coefficients:
$$ \text{coord}_{B}\left(\sum_{i=1}^{n} a_i \vec{b_i}\right) = \sum_{i=1}^{n} a_i \cdot \text{coord}_{B}(\vec{b_i}) = \begin{pmatrix} a_1 \\ a_2 \\ \vdots \\ a_n \end{pmatrix} $$

### Mappings (Functions) and Commutative Diagrams

The latter part of the lecture took a "detour" into the abstract world of [zobrazen-funkce_mc_zobrazení---funkce.md](https://felwiki.basta.one/en/Concepts/zobrazen-funkce_mc_zobrazení---funkce.md) (mappings or functions) and their representation using [komutativn-diagram_mc_komutativní-diagram.md](https://felwiki.basta.one/en/Concepts/komutativn-diagram_mc_komutativní-diagram.md)s. This provides a powerful framework for understanding relationships between mathematical structures.

**Recap of Mappings:**
A [zobrazen-funkce_mc_zobrazení---funkce.md](https://felwiki.basta.one/en/Concepts/zobrazen-funkce_mc_zobrazení---funkce.md) $f: X \to Y$ is formally defined as a subset of the Cartesian product $X \times Y$ such that for every $x \in X$, there exists exactly one $y \in Y$ for which $(x,y) \in f$. This $y$ is denoted as $f(x)$. The lecture also reminded students of the [slo-en-zobrazen_mc_složené-zobrazení.md](https://felwiki.basta.one/en/Concepts/slo-en-zobrazen_mc_složené-zobrazení.md) (composition of mappings): for $f: X \to Y$ and $g: Y \to Z$, the composite map $g \cdot f: X \to Z$ is defined by $(g \cdot f)(x) = g(f(x))$.

**Commutative Diagrams:**
A diagram is said to be [komutativn-diagram_mc_komutativní-diagram.md](https://felwiki.basta.one/en/Concepts/komutativn-diagram_mc_komutativní-diagram.md) if all directed paths between any two objects in the diagram lead to the same result through composition. This concept is visualized with simple shapes:
*   **Commutative Triangle:** A triangle diagram involving mappings $f: X \to Y$, $g: Y \to Z$, and $h: X \to Z$ is commutative if $h = g \cdot f$, meaning $h(x) = g(f(x))$ for all $x \in X$.
*   **Commutative Square:** A square diagram with mappings $f: A \to B$, $g: A \to X$, $h: B \to Y$, and $k: X \to Y$ is commutative if $h \cdot f = k \cdot g$, meaning $h(f(x)) = k(g(x))$ for all $x \in A$.
The lecture also touched upon the "gluing" of commutative diagrams (if parts commute, the combined diagram might also commute) and "tearing" (sub-diagrams of a commutative diagram are not necessarily commutative).

**Types of Mappings:**
The lecture concluded by reviewing important classifications of mappings:
*   A mapping $f: X \to Y$ is [prost-zobrazen-injekce_mc_prosté-zobrazení---injekce.md](https://felwiki.basta.one/en/Concepts/prost-zobrazen-injekce_mc_prosté-zobrazení---injekce.md) (injective or one-to-one) if $f(x_1) = f(x_2)$ implies $x_1 = x_2$.
*   A mapping $f: X \to Y$ is [zobrazen-na-surjekce_mc_zobrazení-na---surjekce.md](https://felwiki.basta.one/en/Concepts/zobrazen-na-surjekce_mc_zobrazení-na---surjekce.md) (surjective or onto) if for every $y \in Y$, there exists an $x \in X$ such that $f(x) = y$.
*   A mapping $f: X \to Y$ is a [bijekce_mc_bijekce.md](https://felwiki.basta.one/en/Concepts/bijekce_mc_bijekce.md) (bijective or one-to-one correspondence) if it is both injective and surjective.

**Identity and Inverse Mappings:**
The identity map $\text{id}_X: X \to X$, defined by $\text{id}_X(x) = x$, is a bijection. Function composition is associative: $h \cdot (g \cdot f) = (h \cdot g) \cdot f$. The identity map acts as a neutral element for composition: $\text{id}_Y \cdot f = f = f \cdot \text{id}_X$.
Finally, a mapping $f: X \to Y$ is a [bijekce_mc_bijekce.md](https://felwiki.basta.one/en/Concepts/bijekce_mc_bijekce.md) if and only if there exists a unique [inverzn-zobrazen_mc_inverzní-zobrazení.md](https://felwiki.basta.one/en/Concepts/inverzn-zobrazen_mc_inverzní-zobrazen.md) (inverse mapping), denoted $f^{-1}: Y \to X$, such that $f^{-1} \cdot f = \text{id}_X$ and $f \cdot f^{-1} = \text{id}_Y$. It was also noted that the composition of injections is an injection, surjections is a surjection, and bijections is a bijection.

### Conclusion

This lecture provided a foundational understanding of how vectors are represented in linear spaces through coordinates relative to an ordered basis, emphasizing the linearity of this coordinate mapping. Simultaneously, it introduced the powerful abstract language of mappings and commutative diagrams, laying the groundwork for understanding more complex linear transformations and their properties in a structured and intuitive way. Students were encouraged to review specific examples in the course textbook to solidify their understanding of these concepts.

**Keywords:** Linear Algebra, Vector Spaces, Ordered Basis, Mappings, Commutative Diagrams, Coordinates, Canonical Basis, Injective, Surjective, Bijective, Inverse Mapping