# Složené zobrazení

## Summary
Given mappings f : X -> Y and g : Y -> Z, their composition (or composite mapping) is denoted g · f : X -> Z and is defined by (g · f)(x) = g(f(x)).

## Detailed Explanation
A **composite mapping** (or **složené zobrazení** in Czech) is a function that takes the output of one function as the input for another function. This effectively chains functions together.

### Definition
According to the provided definition from lecture "Souřadnice vzhledem k uspořádané bázi a komutativní diagramy":
"Given mappings $f : X \rightarrow Y$ and $g : Y \rightarrow Z$, their composition (or composite mapping) is denoted $g \cdot f : X \rightarrow Z$ and is defined by $(g \cdot f)(x) = g(f(x))$."

This means that to apply the composite mapping $g \cdot f$ to an element $x$, one first applies $f$ to $x$ to get $f(x)$, and then applies $g$ to the result $f(x)$ to get $g(f(x))$. For the composition to be well-defined, the codomain of the first function must be the same as the domain of the second function.

## Importance/Relevance
This concept is highly important (Importance Score: 0.8) for understanding how functions can be combined to form more complex operations. It is fundamental in areas like abstract algebra, calculus (chain rule), and computer science.

## Connections
This concept appears in the following lecture:
*   Souřadnice vzhledem k uspořádané bázi a komutativní diagramy

## Category
Operation