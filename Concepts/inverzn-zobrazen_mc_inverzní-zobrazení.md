# Inverzní zobrazení

## Summary
A mapping $f : X \rightarrow Y$ is a bijection if and only if there exists a unique mapping $g : Y \rightarrow X$ (called the inverse mapping, denoted $f^{-1}$) such that $g \circ f = id_X$ (the identity map on $X$) and $f \circ g = id_Y$ (the identity map on $Y$).

## Detailed Explanation
An **inverse mapping** (or inverse function) is a concept intrinsically linked to bijections. For a mapping to have an inverse, it must be a bijection. This means it must be both injective (one-to-one) and surjective (onto).

If a mapping $f : X \rightarrow Y$ is a bijection, then for every element $y$ in the codomain $Y$, there is exactly one element $x$ in the domain $X$ such that $f(x) = y$. This unique relationship allows us to define an inverse mapping that "reverses" the action of $f$.

The inverse mapping, denoted $f^{-1}$, maps elements from $Y$ back to $X$. Specifically, if $f(x) = y$, then $f^{-1}(y) = x$.

### Properties of the Inverse Mapping
The inverse mapping $f^{-1}$ satisfies two crucial properties involving composition with the original mapping $f$:

*   **$g \circ f = id_X$**: Composing $f$ with $f^{-1}$ (where $f$ is applied first) results in the identity map on the domain $X$. This means $f^{-1}(f(x)) = x$ for all $x \in X$.
*   **$f \circ g = id_Y$**: Composing $f^{-1}$ with $f$ (where $f^{-1}$ is applied first) results in the identity map on the codomain $Y$. This means $f(f^{-1}(y)) = y$ for all $y \in Y$.

### Definition
*   "A mapping $f : X \rightarrow Y$ is a bijection if and only if there exists a unique mapping $g : Y \rightarrow X$ (called the inverse mapping, denoted $f^{-1}$) such that $g \circ f = id_X$ (the identity map on $X$) and $f \circ g = id_Y$ (the identity map on $Y$)." (Source: Souřadnice vzhledem k uspořádané bázi a komutativní diagramy)

## Key Aspects/Components
N/A - Specific components are not explicitly detailed in the provided data.

## Importance/Relevance
This concept is highly important (Overall Importance Score: 0.9) as it is fundamental in many areas of mathematics, including linear algebra (for invertible matrices), abstract algebra (for isomorphisms), and calculus (for inverse functions). The existence of an inverse mapping signifies that a transformation is fully reversible without loss of information.

## Connections
### Appears In
*   [Souřadnice vzhledem k uspořádané bázi a komutativní diagramy](lec_3289d167-fa7a-4cac-8687-df4989575e0d)

### Aliases
*   None

## Category
Concept