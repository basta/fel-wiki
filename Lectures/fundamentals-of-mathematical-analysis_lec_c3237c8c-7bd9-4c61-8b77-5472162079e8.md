# Fundamentals of Mathematical Analysis

This lecture provides a comprehensive overview of fundamental concepts in mathematical analysis, laying the groundwork for advanced topics in calculus and real analysis. It systematically introduces various number systems, defines properties of sets of real numbers, delves into the characteristics of functions, explores the crucial concept of limits, and culminates in a detailed discussion of derivatives and their applications through key theorems.

## Foundations: Number Systems and Set Properties

The lecture began by reviewing the foundational **number systems**, essential for understanding real analysis. These include the natural numbers ($\mathbb{N}$), integers ($\mathbb{Z}$), [rational numbers](https://felwiki.basta.one/en/Concepts/racion-ln-sla-rational-numbers) ($\mathbb{Q}$), [real numbers](https://felwiki.basta.one/en/Concepts/re-ln-sla-real-numbers) ($\mathbb{R}$), and [irrational numbers](https://felwiki.basta.one/en/Concepts/iracion-ln-sla-irrational-numbers) ($\mathbb{R} \setminus \mathbb{Q}$). A key assertion highlighted was the irrationality of $\sqrt{2}$. Furthermore, [complex numbers](https://felwiki.basta.one/en/Concepts/komplexn-sla-complex-numbers) were introduced as $C = \{x+iy: x, y \in\mathbb{R}\}$, where $i^2 = -1$.

A significant aspect of real numbers is their [decimal expansion](https://felwiki.basta.one/en/Concepts/decimal-expansion_mc_decimal-expansion), expressed as $\pm a_0,a_1a_2\dots=\pm\sum_{n=0}^{\infty} a_n\cdot10^{-n}$. A crucial property discussed is that rational numbers are precisely those with a finite or periodic decimal expansion. The concept of [extended real numbers](https://felwiki.basta.one/en/Concepts/extended-real-numbers_mc_extended-real-numbers), $\mathbb{R} = \mathbb{R} \cup \{-\infty,+\infty\}$, was also introduced to handle concepts involving infinity.

Following this, the lecture moved to defining [intervals](https://felwiki.basta.one/en/Concepts/intervals_mc_intervals) (open, closed, and half-open) on the real line. A fundamental property of the real numbers, known as [density](https://felwiki.basta.one/en/Concepts/hustota-density_mc_hustota-density), was stated: in every interval, there exist infinitely many rational and irrational numbers.

The discussion then shifted to the properties of sets of real numbers, specifically their **bounds and extrema**. For a set $M \subset \mathbb{R}$:
*   A number $z \in \mathbb{R}$ is an [upper bound](https://felwiki.basta.one/en/Concepts/horn-z-vora-upper-bound) of $M$ if $M \leq z$.
*   A number $z \in \mathbb{R}$ is a [lower bound](https://felwiki.basta.one/en/Concepts/doln-z-vora-lower-bound) of $M$ if $z \leq M$.
*   A set $M$ is [bounded](https://felwiki.basta.one/en/Concepts/omezen-bounded) if it is both bounded above and below.

Beyond simple bounds, the lecture defined key extrema:
*   The maximum of $M$ ($\max M$) is its largest element.
*   The minimum of $M$ ($\min M$) is its smallest element.
*   The [supremum](https://felwiki.basta.one/en/Concepts/supremum-least-upper-bound) of $M$ ($\sup M$) is the least upper bound of $M$.
*   The [infimum](https://felwiki.basta.one/en/Concepts/infimum-greatest-lower-bound) of $M$ ($\inf M$) is the greatest lower bound of $M$.
A critical theorem asserts that every non-empty set of real numbers that is bounded above has a unique supremum, and every non-empty set of real numbers that is bounded below has a unique infimum.

## Functions and Their Characteristics

The lecture then transitioned to the concept of a [function](https://felwiki.basta.one/en/Concepts/funkce-function_mc_funkce-function), defined as a mapping $f: A \to \mathbb{R}$, where $A \subset \mathbb{R}$ is a non-empty domain $D(f)$, and $f(A)$ is the range $R(f)$. Various classifications of functions were introduced:
*   A function is [injective (one-to-one)](https://felwiki.basta.one/en/Concepts/prost-injective-one-to-one) if distinct inputs map to distinct outputs.
*   A function is [surjective (onto)](https://felwiki.basta.one/en/Concepts/na-surjective-onto) if its range equals its codomain.
*   A function is a [bijection](https://felwiki.basta.one/en/Concepts/vz-jemn-jednozna-n-bijection) if it is both injective and surjective.

The concept of an [inverse function](https://felwiki.basta.one/en/Concepts/inverzn-funkce-inverse-function_mc_inverzní-funkce-inverse-function), denoted $f^{-1}$, was defined, with its existence being contingent on the function being injective. If $f$ is injective, then $f^{-1}: R(f) \to A$ exists such that $(f^{-1} \circ f)(x) = x$. A key property is that the graph of $f^{-1}$ is symmetric to the graph of $f$ with respect to the line $y=x$.

**Monotonicity** is another important property of functions:
*   A function $f$ is [monotonic](https://felwiki.basta.one/en/Concepts/monotonn-monotonic-function) if it is consistently increasing ($f(x) < f(y)$ for $x < y$), decreasing ($f(x) > f(y)$ for $x < y$), non-decreasing ($f(x) \leq f(y)$ for $x < y$), or non-increasing ($f(x) \geq f(y)$ for $x < y$). An important theorem states that strictly monotonic functions (increasing or decreasing) are injective, and thus have an inverse function which retains the same monotonicity.

Additional functional properties covered included:
*   [Even functions](https://felwiki.basta.one/en/Concepts/sud-funkce-even-function) where $f(-x) = f(x)$.
*   [Odd functions](https://felwiki.basta.one/en/Concepts/odd-function_mc_odd-function) where $f(-x) = -f(x)$.
*   [Periodic functions](https://felwiki.basta.one/en/Concepts/periodic-function_mc_periodic-function) with period $p > 0$ such that $f(x+p) = f(x)$. The smallest such $p$ (if it exists) is called the fundamental period.

## Limits of Functions

A core concept in mathematical analysis is the [limit of a function](https://felwiki.basta.one/en/Concepts/limit-of-a-function_mc_limit-of-a-function). The lecture introduced the notions of a **neighborhood** $U(a, r) = (a-r, a+r)$ and a **punctured neighborhood** $P(a, r) = U(a, r) \setminus \{a\}$ of a point $a \in \mathbb{R}$ with radius $r$. The formal definition of a limit, $\lim_{x \to a} f(x) = b$, states that for every neighborhood $U$ of $b$, there exists a punctured neighborhood $P$ of $a$ such that $f(P) \subset U$.

The lecture also discussed [one-sided limits](https://felwiki.basta.one/en/Concepts/jednostrann-limita-one-sided-limit), approached from the left (e.g., $x \to a^-$) or right (e.g., $x \to a^+$). A crucial theorem states that for a function $f$ defined in a punctured neighborhood of $a$, $\lim_{x \to a} f(x) = b$ if and only if $\lim_{x \to a^-} f(x) = \lim_{x \to a^+} f(x) = b$.

Several important theorems concerning limits were presented:
*   The [Uniqueness Theorem of Limits](https://felwiki.basta.one/en/Concepts/v-ta-o-jednozna-nosti-uniqueness-theorem-of-limits) states that a function has at most one limit at any given point.
*   The [Monotonicity Theorem for Limits](https://felwiki.basta.one/en/Concepts/v-ta-o-monotonii-limit-monotonicity-theorem-for-limits) establishes that if $f(x) \leq g(x)$ in a punctured neighborhood of $a$, and both $\lim_{x \to a} f(x) = b$ and $\lim_{x \to a} g(x) = c$ exist, then $b \leq c$.
*   Other limit properties include: a function with a finite limit at $a$ is bounded in a punctured neighborhood of $a$; a function with a positive (negative) limit at $a$ is positive (negative) in a punctured neighborhood of $a$; and $\lim_{x \to a} f(x) = 0$ if and only if $\lim_{x \to a} |f(x)| = 0$.
*   Monotonic functions on an open interval have corresponding one-sided limits at their endpoints, equal to the supremum or infimum of their range.
*   The **Algebra of Limits** allows limits of sums, differences, products, and quotients of functions to be computed as the sum, difference, product, and quotient of their individual limits, provided the operations are defined (including operations with extended real numbers).
*   The [Squeeze Theorem](https://felwiki.basta.one/en/Concepts/v-ta-o-sev-en-squeeze-theorem) (or Sandwich Theorem) is a powerful tool: if $f(x) \leq h(x) \leq g(x)$ in a punctured neighborhood of $a$, and $\lim_{x \to a} f(x) = \lim_{x \to a} g(x) = b$, then $\lim_{x \to a} h(x) = b$. A notable application of this theorem yields the special limit:
    $$ \lim_{x\to 0} \frac{\sin x}{x} = 1 $$
*   The lecture also addressed situations involving infinite or non-existent limits, such as cases where $\lim_{x \to a} f(x) = 0$ and $g(x)$ is bounded, leading to $\lim_{x \to a} f(x)g(x) = 0$.
*   Finally, the **Composite Function Limit Theorem** was introduced: if $\lim_{x \to a} f(x) = b$, $\lim_{y \to b} g(y) = c$, and either $f(x) \neq b$ in a punctured neighborhood of $a$ or $g(b)=c$, then $\lim_{x \to a} (g \circ f)(x) = c$.

## Continuity of Functions

Building on the concept of limits, the lecture defined [continuity](https://felwiki.basta.one/en/Concepts/spojit-funkce-continuous-function) as a function $f$ being continuous at a point $a \in D(f)$ if for every neighborhood $U$ of $f(a)$, there exists a neighborhood $V$ of $a$ such that $f(V \cap D(f)) \subset U$. More practically, a function $f$ defined in a neighborhood of $a$ is continuous at $a$ if and only if $\lim_{x \to a} f(x) = f(a)$. A function is simply "continuous" if it is continuous at every point in its domain.

Key properties of continuous functions were discussed:
*   The sum, difference, product, and quotient (if defined) of functions continuous at a point $a$ are also continuous at $a$. The absolute value of a continuous function is also continuous.
*   A function continuous at $a$ is bounded in its neighborhood.
*   If $f$ is continuous at $a$ and $f(a) > 0$, then $f(x) > 0$ in a neighborhood of $a$.
*   The composition of continuous functions is continuous: if $f$ is continuous at $a$ and $g$ is continuous at $f(a)$, then $g \circ f$ is continuous at $a$. As a consequence, rational functions, powers, exponentials, and trigonometric functions (and their inverses) are continuous within their domains.

Two fundamental theorems for continuous functions on intervals were presented:
*   **Weierstrass's Theorem (Extreme Value Theorem)**: A continuous function on a closed interval attains both a maximum and a minimum value on that interval.
*   The [Intermediate Value Theorem](https://felwiki.basta.one/en/Concepts/intermediate-value-theorem-o-mezihodnot) states that if a function $f$ is continuous on an interval and takes on values $m < M$, then it takes on all values within the interval $(m, M)$.
A corollary derived from these concepts is that a continuous function on an interval is injective (and thus has an inverse) if and only if it is strictly monotonic. Furthermore, the [continuity of inverse functions](https://felwiki.basta.one/en/Concepts/inverse-function_mc_inverse-function) is guaranteed if the original function is strictly monotonic on an interval.

## Derivatives and Their Applications

The final part of the lecture focused on the [derivative of a function](https://felwiki.basta.one/en/Concepts/derivative-of-a-function_mc_derivative-of-a-function), which measures the instantaneous rate of change. The derivative $f'(a)$ at a point $a$ is defined as the limit of the difference quotient:
$$ f'(a) = \lim_{h\to 0} \frac{f(a+h)-f(a)}{h} = \lim_{x\to a} \frac{f(x)-f(a)}{x-a} $$
One-sided derivatives (from the left or right) were also mentioned. A critical theorem states that [differentiability implies continuity](https://felwiki.basta.one/en/Concepts/differentiability-implies-continuity-theorem_mc_differentiability-implies-continuity-theorem): if a function has a finite derivative at a point, it is continuous at that point.

The lecture then provided **basic differentiation rules**:
*   The derivative of a constant $c$ is zero: $(c)' = 0$.
*   The power rule: $(x^a)' = ax^{a-1}$.
*   The derivative of the exponential function: $(e^x)' = e^x$.
*   Derivatives of trigonometric functions: $(\sin x)' = \cos x$ and $(\cos x)' = -\sin x$.

Fundamental rules for combining derivatives were also covered:
*   **Sum/Difference Rule**: $(f \pm g)'(a)= f'(a) \pm g'(a)$.
*   **Product Rule**: $(fg)'(a)= f'(a)g(a)+f(a)g'(a)$.
*   **Quotient Rule**: $\left(\frac{f}{g}\right)'(a) = \frac{f'(a)g(a)-f(a)g'(a)}{g(a)^2}$ for $g(a) \neq 0$.
*   The [Chain Rule](https://felwiki.basta.one/en/Concepts/chain-rule_mc_chain-rule) for composite functions: $(g \circ f)'(a)=g'(f(a))\cdot f'(a)$.
*   The **Derivative of the [Inverse Function](https://felwiki.basta.one/en/Concepts/inverse-function_mc_inverse-function)**: if $f$ is continuous and strictly monotonic on an interval $I$, and $f'(a) \neq 0$, then $(f^{-1})'(f(a)) = \frac{1}{f'(a)}$.

The lecture concluded with several pivotal theorems in differential calculus:
*   [Rolle's Theorem](https://felwiki.basta.one/en/Concepts/rolle-s-theorem_mc_rolles-theorem): If $f$ is continuous on $[a,b]$, differentiable on $(a,b)$, and $f(a) = f(b)$, then there exists $c \in (a,b)$ such that $f'(c)=0$.
*   [Lagrange's Mean Value Theorem](https://felwiki.basta.one/en/Concepts/lagrange-s-mean-value-theorem-o-p-r-stku-funkce_mc_lagranges-mean-value-theorem-o-přírůstku-funkce): If $f$ is continuous on $[a,b]$ and differentiable on $(a,b)$, then there exists $c \in (a,b)$ such that $f(b)- f(a) = f'(c)\cdot(b-a)$.
*   [Cauchy's Mean Value Theorem](https://felwiki.basta.one/en/Concepts/cauchy-s-mean-value-theorem_mc_cauchyho-v-ta-cauchys-mean-value-theorem): If $f, g$ are continuous on $[a,b]$ and differentiable on $(a,b)$ with $g'(x) \neq 0$ on $(a,b)$, then there exists $c \in (a,b)$ such that $\frac{f(b)-f(a)}{g(b)-g(a)} = \frac{f'(c)}{g'(c)}$.
*   [L'Hôpital's Rule](https://felwiki.basta.one/en/Concepts/l-h-pital-s-rule_mc_lhôpitals-rule): This powerful rule provides a method for evaluating indeterminate forms of limits. If $\lim_{x \to a^+} f(x)= \lim_{x \to a^+} g(x)=0$ or $\lim_{x \to a^+} |g(x)|=+\infty$, and $\lim_{x \to a^+} \frac{f'(x)}{g'(x)} = b$, then $\lim_{x \to a^+} \frac{f(x)}{g(x)} = b$.

Overall, this lecture provided a thorough introduction to the core concepts of mathematical analysis, building from foundational number systems and set theory through functions, limits, and the fundamental principles of differentiation, equipping students with essential tools for further study in the field.

### Keywords
Mathematics, Calculus, Real Analysis, Functions, Limits