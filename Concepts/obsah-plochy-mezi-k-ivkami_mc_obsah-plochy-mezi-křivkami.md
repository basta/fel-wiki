# Obsah plochy mezi křivkami

## Summary
The area of the region bounded by two piecewise continuous functions $f(x)$ and $g(x)$ over an interval $(a, b)$, where $f(x) \leq g(x)$ for all $x$ in the interval, is calculated by the definite integral of the difference between the upper and lower functions. Specifically, the area is given by $\int_a^b (g(x) - f(x)) dx$. This formula represents the sum of infinitesimally thin vertical strips between the two curves.

## Detailed Explanation
One of the most direct and intuitive applications of definite integrals is to calculate the area of a region bounded by curves. This extends the concept of finding the area under a single curve (which is the area between the curve and the x-axis) to finding the area between two curves.

### Definition:
*   **Definition 1:** For two piecewise continuous functions $f(x)$ and $g(x)$ defined on an interval $(a, b)$, if $f(x) \leq g(x)$ for all $x \in (a, b)$, then the area $A$ of the region $R = \{[x, y]: a < x < b, f(x) \leq y \leq g(x)\}$ is given by the definite integral:
    $$ A = \int_a^b (g(x) - f(x)) dx $$
    Here, $g(x)$ is the "upper" function and $f(x)$ is the "lower" function within the specified interval. The integral effectively sums the heights $(g(x) - f(x))$ of infinitesimally thin vertical rectangles across the interval $(a,b)$.
    *   *Source:* lec_0a0dc037-8067-470a-8948-277889b1ab2d

## Importance/Relevance
This concept is of medium-high importance (overall importance score: 0.7) as a fundamental application of integral calculus. It is widely used in geometry, physics (e.g., calculating work done, volume of solids of revolution), and engineering (e.g., fluid dynamics, stress-strain analysis) to determine quantities that can be represented as areas under or between curves.

## Connections
This concept appears in the lecture:
*   "Mathematical Analysis: Integrals, Series, and Numerical Methods" (lec_0a0dc037-8067-470a-8948-277889b1ab2d)

## Category
Integral Application