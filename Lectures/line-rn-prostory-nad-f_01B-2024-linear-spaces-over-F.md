# Lineární prostory nad F
## Lineární algebra - Lecture 1
**Speaker:** Jiří Velebil

This lecture provides a comprehensive introduction to the concept of **linear spaces over an arbitrary field F**, building upon the foundational ideas of linear spaces over real numbers. The primary goal is to generalize algebraic concepts, demonstrating that many proofs and properties do not depend on the specific nature of real numbers, but rather on their fundamental algebraic characteristics.

### Generalizing from Real Numbers to Fields

The lecture began by revisiting the basic properties of addition and multiplication in the set of [Reálná čísla (Real Numbers)](https://felwiki.basta.one/en/Concepts/re-ln-sla-real-numbers) ($\mathbb{R}$). These properties include the existence of a zero element for addition ($a+0=0+a=a$), associativity of addition (($a+b)+c=a+(b+c)$), commutativity of addition ($a+b=b+a$), and the existence of an opposite element (for any $a \in \mathbb{R}$, there exists $b \in \mathbb{R}$ such that $a+b=0$). For multiplication, properties include the existence of a unity element ($1 \cdot a = a$), associativity ($a \cdot (b \cdot c) = (a \cdot b) \cdot c$), commutativity ($a \cdot b = b \cdot a$), and crucial for the generalization, the **invertibility test**: for any $a \in \mathbb{R}$, $a \ne 0$ if and only if there exists $a^{-1}$ such that $a \cdot a^{-1} = 1$. The interplay between addition and multiplication is governed by the [Distributivní zákony (Distributive Laws)](https://felwiki.basta.one/en/Concepts/distributivn-z-kony-distributive-laws): $a \cdot (b+c) = a \cdot b + a \cdot c$ and $(b+c) \cdot a = b \cdot a + c \cdot a$.

This set of fundamental properties led directly to the formal definition of a **[Těleso (Field)](https://felwiki.basta.one/en/Concepts/t-leso-field)**, which is essentially any set F equipped with two binary operations (addition `+` and multiplication `•`) that satisfy all these axioms. The lecture emphasized that a field is a collection of objects (called elements or [skaláry (scalar)](https://felwiki.basta.one/en/Concepts/skal-r)) that can be added and multiplied in a way that mimics the behavior of real numbers.

Examples of fields include:
*   [Racionální čísla (Rational Numbers)](https://felwiki.basta.one/en/Concepts/racion-ln-sla-rational-numbers) ($\mathbb{Q}$) with standard operations.
*   [Reálná čísla (Real Numbers)](https://felwiki.basta.one/en/Concepts/re-ln-sla-real-numbers) ($\mathbb{R}$) with standard operations.
*   [Komplexní čísla (Complex Numbers)](https://felwiki.basta.one/en/Concepts/komplexn-sla-complex-numbers) ($\mathbb{C}$) with standard operations.

It was highlighted that the set of integers ($\mathbb{Z}$) is *not* a field under standard addition and multiplication, primarily because it fails the invertibility test (e.g., $2 \ne 0$ but $2^{-1}$ does not exist in $\mathbb{Z}$). This means that $\mathbb{Z}$ cannot serve as the set of [skaláry (scalar)](https://felwiki.basta.one/en/Concepts/skal-r) for a linear space.

Interestingly, the lecture also introduced "non-standard" examples of fields: $\mathbb{Z}_2 = \{0, 1\}$ and $\mathbb{Z}_3 = \{0, 1, 2\}$, where addition and multiplication are performed modulo 2 and 3, respectively. For instance, in $\mathbb{Z}_2$, $1+1=0$ and $1 \cdot 1 = 1$. It was noted that generally, $\mathbb{Z}_p = \{0, 1, \dots, p-1\}$ forms a field if $p$ is a prime number, with operations defined modulo $p$. These examples underscore that the abstract definition of a field is not limited to familiar number systems.

### Defining Linear Spaces over an Arbitrary Field

With the concept of a field established, the lecture proceeded to define a **[Lineární prostor nad tělesem F (Linear Space over Field F / Vector Space over Field F)](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-t-lesem-f-linear-space-over-field-f---vector-space-over-field-f)**. This definition is formally identical to that of a [Lineární prostor nad R](https://felwiki.basta.one/en/Concepts/line-rn-prostor-nad-r), with the only change being that the field of real numbers $\mathbb{R}$ is replaced by a general field $F$.

A linear space $L$ over a field $F$ is a set of elements called [vektory (vector)](https://felwiki.basta.one/en/Concepts/vektor), equipped with two operations:
1.  **Vector Addition (+ : $L \times L \rightarrow L$):**
    *   Existence of a unique [Nulový vektor (Zero Vector)](https://felwiki.basta.one/en/Concepts/nulov-vektor-zero-vector) $\vec{0}$ such that for all $\vec{x} \in L$, $\vec{x} + \vec{0} = \vec{0} + \vec{x} = \vec{x}$.
    *   Associativity: $(\vec{x} + \vec{y}) + \vec{z} = \vec{x} + (\vec{y} + \vec{z})$.
    *   Commutativity: $\vec{x} + \vec{y} = \vec{y} + \vec{x}$.
    *   Existence of an [Opačný vektor (Opposite Vector)](https://felwiki.basta.one/en/Concepts/opa-n-vektor-opposite-vector) for each $\vec{x} \in L$, denoted $-\vec{x}$, such that $\vec{x} + (-\vec{x}) = \vec{0}$.
2.  **Scalar Multiplication (• : $F \times L \rightarrow L$):**
    *   Multiplication by the unity scalar: $1 \cdot \vec{x} = \vec{x}$ for all $\vec{x} \in L$.
    *   Associativity of scalar multiplication: $a \cdot (b \vec{x}) = (a \cdot b) \cdot \vec{x}$ for all $a, b \in F$ and $\vec{x} \in L$.
    *   Distributivity of scalar sum over vector: $(a+b) \cdot \vec{x} = a \cdot \vec{x} + b \cdot \vec{x}$.
    *   Distributivity of scalar over vector sum: $a \cdot (\vec{x} + \vec{y}) = a \cdot \vec{x} + a \cdot \vec{y}$.

Several simple, yet important, consequences of these axioms were then derived:
*   The [Nulový vektor (Zero Vector)](https://felwiki.basta.one/en/Concepts/nulov-vektor-zero-vector) is unique.
*   For any $\vec{x} \in L$, $0 \cdot \vec{x} = \vec{0}$.
*   The [Opačný vektor (Opposite Vector)](https://felwiki.basta.one/en/Concepts/opa-n-vektor-opposite-vector) of $\vec{x}$ is precisely $(-1) \cdot \vec{x}$.
*   For any $a \in F$, $a \cdot \vec{0} = \vec{0}$.
*   A crucial result: $a \cdot \vec{x} = \vec{0}$ if and only if $a=0$ or $\vec{x}=\vec{0}$. These proofs are identical to those for linear spaces over $\mathbb{R}$, reinforcing the power of abstraction.

Examples of linear spaces over a general field $F$ include:
*   $F^n$: The set of ordered $n$-tuples of elements from $F$, written as column vectors. For example, vectors in $(\mathbb{Z}_7)^2$ or $\mathbb{Q}^3$.
*   $F[x]$: The set of polynomials in an indeterminate $x$ with [koeficienty (coefficients)](https://felwiki.basta.one/en/Concepts/koeficienty-line-rn-kombinace-coefficients-of-a-linear-combination) from field $F$. Addition and multiplication are defined analogously to polynomials over $\mathbb{R}$. For instance, in $\mathbb{Z}_3[x]$, $(2x+2) + (x+2) = 1$ and $(2x+2) \cdot (x+2) = 2x^2+1$.

### Linear Combinations

The most general computation that can be performed in a linear space is forming a **[Lineární kombinace (Linear Combination)](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-linear-combination)**. Given a finite list of [vektory (vector)](https://felwiki.basta.one/en/Concepts/vektor) $(\vec{x}_1, \dots, \vec{x}_n)$ from $L$ and a finite list of [skaláry (scalar)](https://felwiki.basta.one/en/Concepts/skal-r) (coefficients) $(a_1, \dots, a_n)$ from $F$, a linear combination is expressed as:
$$a_1\vec{x}_1 + a_2\vec{x}_2 + a_3\vec{x}_3 + \dots + a_n\vec{x}_n \quad \text{or} \quad \sum_{i=1}^{n} a_i \vec{x}_i$$
The lecture clarified the distinction between a *list* (or group) of vectors, where order and repetition matter, and a *set* of vectors. For an empty list of vectors, the (only possible) linear combination is defined as the [Nulový vektor (Zero Vector)](https://felwiki.basta.one/en/Concepts/nulov-vektor-zero-vector).

The geometric significance of linear combinations was illustrated:
*   For a single [vektor (vector)](https://felwiki.basta.one/en/Concepts/vektor) $\vec{a}_1$ in $\mathbb{R}^2$, all possible linear combinations (e.g., $2.5 \vec{a}_1$) form a line passing through the origin in the direction of $\vec{a}_1$.
*   For a list of two [vektory (vector)](https://felwiki.basta.one/en/Concepts/vektor) $(\vec{a}_1, \vec{a}_2)$ in $\mathbb{R}^3$, all possible linear combinations (e.g., $2.1 \vec{a}_1 + 1.3 \vec{a}_2$) form a plane passing through the origin, defined by the directions of $\vec{a}_1$ and $\vec{a}_2$ (assuming they are not collinear).

These "straight pieces" of a linear space, formed by linear combinations, will be formally introduced as **linear subspaces** in the next lecture.

### Connection to Systems of Linear Equations

A practical application of linear combinations was demonstrated through the connection to **[Soustava lineárních rovnic](https://felwiki.basta.one/en/Concepts/soustava-line-rn-ch-rovnic)**. The question, "Do coefficients $x, y \in \mathbb{Z}_7$ exist such that in $(\mathbb{Z}_7)^2$, $x \cdot (2,3) + y \cdot (6,1) = (2,6)$?", directly translates into a system of linear equations:
$$
\begin{cases}
2x + 6y = 2 \\
3x + 1y = 6
\end{cases}
$$
The lecture emphasized that finding the [Koeficienty lineární kombinace (Coefficients of a Linear Combination)](https://felwiki.basta.one/en/Concepts/koeficienty-line-rn-kombinace-coefficients-of-a-linear-combination) of given [vektory (vector)](https://felwiki.basta.one/en/Concepts/vektor) to reach a target vector is equivalent to solving a system of linear equations. This dual perspective is crucial for understanding and developing elegant solution methods, such as **[Gaussova eliminační metoda (Gaussian Elimination Method / GEM)](https://felwiki.basta.one/en/Concepts/gaussova-elimina-n-metoda-gem)**, which will be covered in upcoming lectures. The abstract algebraic framework developed in this lecture allows for a unified approach to these problems across different underlying fields.

### Conclusion and Future Outlook

This lecture successfully generalized the concept of a linear space from being defined over the familiar [Reálná čísla (Real Numbers)](https://felwiki.basta.one/en/Concepts/re-ln-sla-real-numbers) to being defined over any arbitrary [Těleso (Field)](https://felwiki.basta.one/en/Concepts/t-leso-field). By focusing on the fundamental algebraic properties rather than specific number systems, the lecture laid the groundwork for a more abstract and powerful linear algebra. Key takeaways include the strict definition of a field, the axioms of a linear space, the concept of a [Lineární kombinace (Linear Combination)](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-linear-combination) and its geometric interpretation, and the fundamental link between linear combinations and [Soustava lineárních rovnic](https://felwiki.basta.one/en/Concepts/soustava-line-rn-ch-rovnic). Future lectures will delve into linear subspaces and efficient methods for solving systems of linear equations based on this generalized framework.

**Keywords:** LinearAlgebra, VectorSpaces, Fields, LinearCombinations, Axioms