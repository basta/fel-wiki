# Integral Calculus: Formulas, Theorems, and Applications

This lecture provides a comprehensive overview of integral calculus, commencing with the fundamental concepts of indefinite integration and progressing to sophisticated techniques and theoretical underpinnings. The discussion thoroughly defines various integral forms, explores methods for their computation, and delves into the properties and applications of both definite and improper integrals.

## Foundations of Indefinite Integration

The lecture began by establishing the basic building blocks of integral calculus: the fundamental indefinite integral formulas. These foundational rules allow us to find the [Primitive function](https://felwiki.basta.one/en/Concepts/primitive-function_mc_primitive-function) (or antiderivative) of common functions. A primitive function $F$ of a given function $f$ on an interval $I$ is a function whose derivative $F'$ equals $f$ on $I$.

Key formulas introduced include:

*   The power rule for integration: $\int x^a dx = \frac{x^{a+1}}{a+1} + c$, valid for $a \ne -1$. Here, $x$ is the variable of integration, $a$ is a constant, and $c$ is the constant of integration.
*   The logarithm rule: $\int \frac{dx}{x} = \ln|x| + c$, for $x \ne 0$.
*   The exponential rule: $\int e^{ax} dx = \frac{1}{a} e^{ax} + c$, for $a \ne 0$.
*   Trigonometric integrals: $\int \sin(ax) dx = -\frac{1}{a} \cos(ax) + c$ and $\int \cos(ax) dx = \frac{1}{a} \sin(ax) + c$, both for $a \ne 0$.
*   The arctangent rule: $\int \frac{dx}{x^2+1} = \text{arctg}(x) + c$.

Furthermore, the lecture highlighted the linearity of integration, stating that if $F_1, \ldots, F_n$ are primitive functions to $f_1, \ldots, f_n$ respectively on an interval $I$, and $c_1, \ldots, c_n$ are real constants, then $c_1 F_1 + \ldots + c_n F_n$ is a primitive function to $c_1 f_1 + \ldots + c_n f_n$ on $I$.

## Essential Integration Techniques

To tackle more complex integrals, two powerful techniques were introduced: [Integration by parts](https://felwiki.basta.one/en/Concepts/integration-by-parts_mc_integration-by-parts) and the [Substitution rule](https://felwiki.basta.one/en/Concepts/substitution-rule_mc_substitution-rule).

### Integration by Parts

The formula for integration by parts is given by:
$$ \int uv' dx = uv - \int u'v dx $$
This technique is particularly useful for integrating products of functions, where $u$ and $v$ are functions of $x$, and $u'$ and $v'$ are their respective derivatives. Its application requires careful selection of which function to designate as $u$ and which as $v'$.

### Substitution Rule

The substitution rule provides a method for simplifying integrals by changing the variable of integration. Two forms of this rule were presented:

1.  If $F$ is a primitive function of $f$, and $\varphi$ is a differentiable function, then:
    $$ \int f(\varphi(t)) \varphi'(t) dt = F(\varphi(t)) + c $$
    This form is used when the integrand directly matches the structure $f(\varphi(t)) \varphi'(t)$.
2.  If $\varphi$ is a bijective (one-to-one and onto) mapping, and $G$ is a primitive function of $f(\varphi(t))\varphi'(t)$, then:
    $$ \int f(x) dx = G(\varphi^{-1}(x)) + c $$
    This second form is useful when starting with an integral in terms of $x$ and transforming it using an inverse substitution.

## Integration of Rational Functions

A significant portion of the lecture focused on integrating [Rational function](https://felwiki.basta.one/en/Concepts/rational-function_mc_rational-function)s, defined as a ratio of two polynomials $P/Q$, where $Q$ is non-zero. A special case is a [Proper rational function](https://felwiki.basta.one/en/Concepts/proper-rational-function_mc_proper-rational-function), where the degree of the numerator $P$ is strictly less than the degree of the denominator $Q$.

The core strategy for integrating rational functions involves decomposing them into [Partial fractions](https://felwiki.basta.one/en/Concepts/partial-fractions_mc_partial-fractions). This method relies on the theorem that any non-zero polynomial can be uniquely factored into linear and irreducible quadratic factors (a concept known as [Polynomial decomposition](https://felwiki.basta.one/en/Concepts/polynomial-decomposition_mc_polynomial-decomposition)). Partial fractions take specific forms:
*   For a linear factor $(x-a)^n$ in the denominator: $\frac{A}{(x-a)^n}$, where $A$ is a constant and $a$ is a real root.
*   For an irreducible quadratic factor $(x^2+px+q)^n$ in the denominator (where $p^2-4q < 0$): $\frac{Ax+B}{(x^2+px+q)^n}$, where $A, B$ are constants.

The systematic steps for integrating rational functions were outlined as:
1.  **Polynomial Division:** If the function is not a proper rational function, divide the numerator by the denominator to obtain a polynomial and a proper rational function.
2.  **Denominator Decomposition:** Factorize the denominator into its linear and irreducible quadratic factors.
3.  **Partial Fraction Expansion:** Write the proper rational function as a sum of partial fractions corresponding to the factors found in step 2.
4.  **Coefficient Determination:** Determine the unknown coefficients in the partial fractions. Once decomposed, each partial fraction can be integrated using standard techniques.

## The Riemann Integral

The lecture transitioned to the [Riemann integral](https://felwiki.basta.one/en/Concepts/riemann-integral_mc_riemann-integral), a fundamental concept for defining the definite integral of a function over a closed interval $[a, b]$. This integral quantifies the signed area under a curve.

The definition of the Riemann integral relies on partitioning the interval $[a, b]$ into smaller subintervals. For a bounded function $f$ on $(a,b)$ and a partition $D = \{x_0, x_1, \ldots, x_n\}$ where $a = x_0 < x_1 < \ldots < x_n = b$:

*   The [Lower integral sum](https://felwiki.basta.one/en/Concepts/lower-integral-sum_mc_lower-integral-sum) for $f$ and $D$ is $S(f, D) = \sum_{i=1}^{n} \inf_{x \in (x_{i-1}, x_i)} f(x) \cdot (x_i - x_{i-1})$.
*   The [Upper integral sum](https://felwiki.basta.one/en/Concepts/upper-integral-sum_mc_upper-integral-sum) for $f$ and $D$ is $S(f, D) = \sum_{i=1}^{n} \sup_{x \in (x_{i-1}, x_i)} f(x) \cdot (x_i - x_{i-1})$.

The Riemann integral of $f$ on $(a, b)$ exists if the supremum of all lower integral sums equals the infimum of all upper integral sums. This common value is the definite integral. A key criterion for the existence of the Riemann integral is that the difference between the upper and lower sums can be made arbitrarily small for a sufficiently fine partition.

Important theorems concerning the existence of the Riemann integral were presented:
*   Monotonic functions on a closed interval are Riemann integrable.
*   Continuous functions on a closed interval are Riemann integrable. This is a powerful result, often relying on the concept of uniform continuity.

## Properties of Definite Integrals

Several essential properties govern the behavior of definite integrals, facilitating their manipulation and computation:

*   **Linearity:**
    *   $\int_{a}^{b} cf dx = c \int_{a}^{b} f dx$ (A constant factor can be pulled out of the integral).
    *   $\int_{a}^{b} (f+g) dx = \int_{a}^{b} f dx + \int_{a}^{b} g dx$ (The integral of a sum is the sum of the integrals).
*   **Monotonicity:** If $f \le g$ on $(a, b)$, then $\int_{a}^{b} f dx \le \int_{a}^{b} g dx$.
*   **Absolute Value Inequality:** $|\int_{a}^{b} f dx| \le \int_{a}^{b} |f| dx$.
*   **Additivity over Intervals:** If $a < b < c$, then $\int_{a}^{c} f dx = \int_{a}^{b} f dx + \int_{b}^{c} f dx$.
*   **Integral over a Point:** $\int_{a}^{a} f dx = 0$.
*   **Reversing Limits:** For $a < b$, $\int_{b}^{a} f dx = -\int_{a}^{b} f dx$.

## Fundamental Theorem of Calculus and Improper Integrals

The lecture culminated with the **[Newton-Leibniz formula](https://felwiki.basta.one/en/Concepts/newton-leibniz-formula_mc_newton-leibniz-formula)**, also known as the Fundamental Theorem of Calculus, which provides a powerful link between differentiation and integration. It states that if $f$ is a bounded function on $(a, b)$ for which the definite integral exists, and $F$ is any primitive function of $f$ on $(a, b)$, then:
$$ \int_{a}^{b} f(x)dx = [F(x)]_{a}^{b} = F(b-) - F(a+) $$
This theorem allows the direct calculation of definite integrals by evaluating the primitive function at the limits of integration.

A key prerequisite for this theorem is the existence of the primitive function, which is guaranteed if the function is continuous. Specifically, if $F(x) = \int_{a}^{x} f(t) dt$ for $x \in (a, b)$, then $F$ is continuous, and $F'(x) = f(x)$ at points where $f$ is continuous. This implies that any continuous function on an interval possesses a primitive function.

The lecture then extended the concept of integration to [Improper integral](https://felwiki.basta.one/en/Concepts/improper-integrals_mc_improper-integrals)s. These integrals are defined when the interval of integration is unbounded (e.g., from $a$ to $\infty$) or when the function itself is unbounded within the interval (e.g., at an endpoint). An improper integral is defined as a limit of proper integrals:
$$ \int_{a}^{b} f(x)dx = \lim_{c\to a^+} \int_{c}^{e} f(x)dx + \lim_{d\to b^-} \int_{e}^{d} f(x)dx $$
where $e$ is an arbitrary point within $(a, b)$. If this limit is finite, the improper integral is said to [Convergence of improper integrals](https://felwiki.basta.one/en/Concepts/convergence-of-improper-integrals_mc_convergence-of-improper-integrals).

Important theorems related to the convergence of improper integrals include:
1.  If $f \le g$ on $(a, b)$ and $\int_{a}^{b} f = +\infty$ (and $g$ is piecewise continuous), then $\int_{a}^{b} g = +\infty$. This is a comparison test for divergence.
2.  If $|f| \le g$ on $(a, b)$ and $\int_{a}^{b} g$ converges (and $f$ is piecewise continuous), then $\int_{a}^{b} f$ also converges. This is a comparison test for convergence.

In summary, this lecture provided a thorough treatment of integral calculus, from basic formulas and techniques to the rigorous definitions of definite integrals and the complexities of improper integrals, emphasizing their theoretical foundations and practical applications.

### Keywords
Integral Calculus, Integration, Riemann Integral, Improper Integral, Theorems