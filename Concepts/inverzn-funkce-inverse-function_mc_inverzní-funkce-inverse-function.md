# Inverzní funkce (Inverse Function)

## Summary
For a function $f: A \to B$, an inverse function $f^{-1}: R(f) \to A$ exists if and only if $f$ is injective. It satisfies $(f^{-1} \circ f)(x) = x$.

## Detailed Explanation
An **inverzní funkce** (or **inverse function**) essentially "reverses" the action of the original function. If a function $f$ maps an element $x$ from its domain $A$ to an element $y$ in its codomain $B$ (i.e., $f(x) = y$), then its inverse function, denoted $f^{-1}$, maps $y$ back to $x$ (i.e., $f^{-1}(y) = x$).

A critical condition for an inverse function to exist is that the original function must be **injective** (one-to-one). If $f$ is injective, it ensures that each output $y$ in the range $R(f)$ corresponds to a unique input $x$. Without injectivity, an output $y$ could come from multiple inputs, and the inverse wouldn't be uniquely defined.

The inverse function $f^{-1}$ operates on the range of $f$, $R(f)$, and maps it back to the domain $A$. The fundamental property of an inverse function is that its composition with the original function yields the identity function. Specifically, for all $x$ in the domain of $f$:
$$ (f^{-1} \circ f)(x) = f^{-1}(f(x)) = x $$
And for all $y$ in the range of $f$:
$$ (f \circ f^{-1})(y) = f(f^{-1}(y)) = y $$

*   **Definition from "Fundamentals of Mathematical Analysis"**: For a function $f: A \to B$, an inverse function $f^{-1}: R(f) \to A$ exists if and only if $f$ is injective. It satisfies $(f^{-1} \circ f)(x) = x$.

## Importance/Relevance
This concept is highly important (score: 0.8) in mathematics, particularly in calculus, linear algebra, and discrete mathematics. Inverse functions are vital for solving equations, transforming coordinate systems, and understanding the reversibility of mathematical operations.

## Connections
This concept appears in the lecture series:
*   "Fundamentals of Mathematical Analysis"

## Category
Function Property