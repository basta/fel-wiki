# Fundamentals of Integral Calculus and Integration Techniques

This lecture provides a comprehensive overview of fundamental concepts and techniques in integral calculus, guiding students from basic indefinite integrals through advanced integration methods, defining the definite (Riemann) integral, and concluding with a discussion of improper integrals. The aim is to equip learners with a solid understanding of antiderivatives, their properties, and applications in calculating areas and handling functions over unbounded domains.

The lecture begins by introducing the **basic indefinite integral formulas**, which form the building blocks for calculating [primitive functions](https://felwiki.basta.one/en/Concepts/primitive-function) (antiderivatives). Key formulas covered include:

*   The power rule: $\int x^a dx = \frac{x^{a+1}}{a+1} + c$, valid for $a \ne -1$.
*   The integral of reciprocal x: $\int \frac{dx}{x} = \ln|x| + c$.
*   Integrals of exponential and trigonometric functions: $\int e^{ax} dx = \frac{1}{a} e^{ax} + c$, $\int \sin(ax) dx = -\frac{1}{a} \cos(ax) + c$, and $\int \cos(ax) dx = \frac{1}{a} \sin(ax) + c$.
*   The integral of $1/(x^2+1)$: $\int \frac{dx}{x^2+1} = \text{arctg } x + c$.

Beyond these basic forms, the lecture delves into crucial **integration techniques**. A fundamental theorem states that if $F_1, \dots, F_n$ are [primitive functions](https://felwiki.basta.one/en/Concepts/primitive-function) for $f_1, \dots, f_n$ on an interval $I$, then any linear combination $c_1 F_1 + \dots + c_n F_n$ is a [primitive function](https://felwiki.basta.one/en/Concepts/primitive-function) for $c_1 f_1 + \dots + c_n f_n$ on $I$.

The lecture then presents two essential techniques:

1.  **[Integration by Parts](https://felwiki.basta.one/en/Concepts/integration-by-parts)**: This powerful method allows for integrating products of functions. The formula states that if $v'$ and $\int u'v$ exist on interval $I$, then $\int uv' = uv - \int u'v$ on $I$.
2.  **[Substitution Rule](https://felwiki.basta.one/en/Concepts/substitution-rule)**: This technique simplifies integrals by changing the integration variable. It is presented in two forms:
    *   Type 1: $\int f(\varphi(t))\varphi'(t) dt = F(\varphi(t)) + c$, where $F$ is a primitive function of $f$. This is used when the integrand is a composite function multiplied by the derivative of its inner function.
    *   Type 2: $\int f(x) dx = G(\varphi^{-1}(x)) + c$, applicable when $\varphi$ is an injective mapping and $G$ is a primitive function of $f(\varphi(t))\varphi'(t)$. This is often used for trigonometric or other complex substitutions.

A significant portion of the lecture is dedicated to the **integration of [rational functions](https://felwiki.basta.one/en/Concepts/rational-function)**. A [rational function](https://felwiki.basta.one/en/Concepts/rational-function) is defined as a quotient of two polynomials, $P/Q$, where $Q$ is non-zero. A [proper rational function](https://felwiki.basta.one/en/Concepts/proper-rational-function) is a special case where the degree of the numerator polynomial $P$ is less than the degree of the denominator polynomial $Q$.

The core technique for integrating rational functions involves **[partial fractions](https://felwiki.basta.one/en/Concepts/partial-fractions) decomposition**. The lecture explains that a non-zero polynomial can be uniquely factored into linear and irreducible quadratic factors. Correspondingly, any [rational function](https://felwiki.basta.one/en/Concepts/rational-function) can be uniquely decomposed into a sum of a polynomial (if it's not a [proper rational function](https://felwiki.basta.one/en/Concepts/proper-rational-function)) and [partial fractions](https://felwiki.basta.one/en/Concepts/partial-fractions). These [partial fractions](https://felwiki.basta.one/en/Concepts/partial-fractions) take specific forms: $A/(x-a)^n$ for linear factors and $(Ax+B)/(x^2+px+q)^n$ for irreducible quadratic factors (where $p^2-4q < 0$).

The practical steps for integrating rational functions are clearly laid out:
1.  **Polynomial Division**: If the function is not a [proper rational function](https://felwiki.basta.one/en/Concepts/proper-rational-function), perform polynomial long division to obtain a polynomial and a [proper rational function](https://felwiki.basta.one/en/Concepts/proper-rational-function).
2.  **Denominator Factorization**: Factorize the denominator of the [proper rational function](https://felwiki.basta.one/en/Concepts/proper-rational-function) into its irreducible linear and quadratic factors.
3.  **[Partial Fractions](https://felwiki.basta.one/en/Concepts/partial-fractions) Expansion**: Write out the partial fraction decomposition with unknown coefficients.
4.  **Coefficient Determination**: Solve for the unknown coefficients.

The lecture also briefly touches on integration formulas involving roots, such as $\int R\left(x, \sqrt[n]{\frac{ax+b}{cx+d}}\right) dx$, which can be simplified using the substitution $t = \sqrt[n]{\frac{ax+b}{cx+d}}$. Additionally, general forms for integrals involving square roots of quadratic terms, like $\int R(x, \sqrt{\pm x^2 \pm a^2}) dx$, are mentioned, implying specific substitution strategies for these cases.

The second major part of the lecture focuses on **definite (Riemann) integrals**. The [Riemann Integral](https://felwiki.basta.one/en/Concepts/riemann-integral) is rigorously defined using integral sums:
*   **Lower Integral Sum**: $S(f, D) = \sum_{i=1}^n \inf f((x_{i-1}, x_i)) \cdot (x_i - x_{i-1})$
*   **Upper Integral Sum**: $\overline{S}(f, D) = \sum_{i=1}^n \sup f((x_{i-1}, x_i)) \cdot (x_i - x_{i-1})$

A function $f$ is Riemann integrable on $[a,b]$ if the supremum of its lower integral sums equals the infimum of its upper integral sums over all possible partitions $D$ of the interval. This common value is the definite integral $\int_a^b f(x)dx$.

The lecture provides key existence theorems for the [Riemann Integral](https://felwiki.basta.one/en/Concepts/riemann-integral):
*   A bounded function $f$ on $(a, b)$ is Riemann integrable if and only if there exists a sequence of partitions $(D_n)$ such that $\lim_{n \to \infty} S(f, D_n) = \lim_{n \to \infty} \overline{S}(f, D_n)$, or equivalently, $\lim_{n \to \infty} (\overline{S}(f, D_n) - S(f, D_n)) = 0$.
*   **[Monotonic functions](https://felwiki.basta.one/en/Concepts/monotonic-function)** on a closed interval are guaranteed to have a definite integral.
*   **[Continuous functions](https://felwiki.basta.one/en/Concepts/spojitá-funkce-continuous-function)** on a closed interval are also guaranteed to have a definite integral, a powerful result stemming from uniform continuity.

Several important properties of definite integrals are highlighted:
*   Linearity: $\int_a^b cf(x) dx = c \int_a^b f(x) dx$ and $\int_a^b (f(x)+g(x)) dx = \int_a^b f(x) dx + \int_a^b g(x) dx$.
*   Monotonicity: If $f \le g$ on $(a, b)$, then $\int_a^b f \le \int_a^b g$.
*   Triangle Inequality: $\left| \int_a^b f \right| \le \int_a^b |f|$.
*   Interval Additivity: For $a < b < c$, $\int_a^c f = \int_a^b f + \int_b^c f$.
*   Zero-length interval: $\int_a^a f = 0$.
*   Swapped limits: $\int_b^a f = -\int_a^b f$ for $a<b$.

The lecture culminates with the **[Fundamental Theorem of Calculus](https://felwiki.basta.one/en/Concepts/fundamental-theorem-of-calculus)**, which establishes a profound connection between differentiation and integration. The first part states that if $F(x) = \int_a^x f(t) dt$, then $F$ is continuous, and $F'(x) = f(x)$ at points where $f$ is continuous. A significant corollary is that any [continuous function](https://felwiki.basta.one/en/Concepts/spojitá-funkce-continuous-function) on an interval possesses a [primitive function](https://felwiki.basta.one/en/Concepts/primitive-function).

This leads directly to the **[Newton-Leibniz Formula](https://felwiki.basta.one/en/Concepts/newton-leibniz-formula)**, a cornerstone of integral calculus:
$$ \int_a^b f(x)dx = [F(x)]_a^b = F(b-) - F(a+) $$
where $F$ is any [primitive function](https://felwiki.basta.one/en/Concepts/primitive-function) of $f$ on $(a,b)$. This formula provides a practical method for evaluating definite integrals by finding an antiderivative and evaluating it at the limits of integration. Newton's integral, $(N)-\int_a^b f = F(b-) - F(a+)$, is also presented as a generalized form.

Finally, the lecture introduces **[improper integrals](https://felwiki.basta.one/en/Concepts/improper-integral)**, which extend the concept of definite integration to cases where the function is unbounded or the interval of integration is unbounded. An [improper integral](https://felwiki.basta.one/en/Concepts/improper-integral) $\int_a^b f(x)dx$ is defined as the sum of limits of definite integrals:
$$ \int_a^b f(x)dx = \lim_{c\to a^+} \int_c^e f(x)dx + \lim_{d\to b^-} \int_e^d f(x)dx $$
If this expression yields a finite value, the integral is said to converge.
The lecture concludes by discussing theorems on the [convergence of improper integrals](https://felwiki.basta.one/en/Concepts/convergence-of-improper-integrals):
*   If $f \le g$ on $(a, b)$ and $\int_a^b f$ diverges to $+\infty$, and $g$ is piecewise continuous, then $\int_a^b g$ also diverges to $+\infty$.
*   If $|f| \le g$ on $(a, b)$ and $\int_a^b g$ converges, and $f$ is piecewise continuous, then $\int_a^b f$ converges. These comparison tests are crucial for determining the convergence or divergence of [improper integrals](https://felwiki.basta.one/en/Concepts/improper-integral).

The lecture thus provides a comprehensive foundation in integral calculus, covering core definitions, techniques, and theorems essential for further study and application in mathematics and related fields.

### Keywords
Calculus, Integration, Primitive Function, Definite Integral, Improper Integral, Partial Fractions