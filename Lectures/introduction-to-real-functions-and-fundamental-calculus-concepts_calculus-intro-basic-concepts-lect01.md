# Introduction to Real Functions and Fundamental Calculus Concepts

This lecture provides a foundational overview of core concepts in real analysis and introductory calculus, aiming to equip students with a solid understanding of number systems, functions, limits, continuity, and derivatives. It covers essential definitions, properties, and fundamental theorems that are critical for further study in mathematics.

## Foundations of Real Numbers

The lecture commenced by defining various fundamental [number systems](https://felwiki.basta.one/en/Concepts/re-ln-sla-real-numbers_mc_reálná-čísla-real-numbers), starting with natural (N), integer (Z), rational (Q), and real (R) numbers. It also explicitly introduced irrational numbers, denoted as R\\Q, and complex numbers (C), defined as $C = \{x+iy: x, y \in R\}$ where $i^2 = -1$. A key assertion highlighted was the irrationality of $\sqrt{2}$.

A crucial distinction within the real number system was made regarding their [decimal expansion](https://felwiki.basta.one/en/Concepts/decimal-expansion_mc_decimal-expansion). [Rational numbers](https://felwiki.basta.one/en/Concepts/racion-ln-sla-rational-numbers_mc_racionální-čísla-rational-numbers) are precisely those that possess a finite or periodic decimal representation. The discussion then moved to [intervals](https://felwiki.basta.one/en/Concepts/intervaly-intervals_mc_intervaly-intervals) in R, categorizing them as open $(a, b) = \{x \in R: a < x < b\}$, closed $[a, b] = \{x \in R : a \le x \le b\}$, and half-open/closed types. An important theorem emphasized the [density](https://felwiki.basta.one/en/Concepts/hustota-density_mc_hustota-density) of both rational and irrational numbers within any given interval. To complete the numerical landscape, the lecture introduced the [extended real numbers](https://felwiki.basta.one/en/Concepts/roz-en-mno-ina-re-ln-ch-sel-extended-real-numbers_mc_rozšířená-množina-reálných-čísel-extended-real-numbers), $\bar{R} = R \cup \{-\infty, +\infty\}$.

Furthermore, the lecture explored concepts related to the [bounds (supremum & infimum)](https://felwiki.basta.one/en/Concepts/bounds-supremum--infimum_mc_bounds-supremum--infimum) of a set $M \subset R$. An upper bound $z$ means $M \le z$, while a lower bound $z$ means $z \le M$. A set is considered bounded if it has both an upper and lower bound. The **Supremum (sup M)** was defined as the least upper bound, and the **Infimum (inf M)** as the greatest lower bound. A fundamental theorem states that every set of real numbers has a unique supremum and infimum.

## Introduction to Real Functions

The heart of the lecture transitioned into the study of [real functions](https://felwiki.basta.one/en/Concepts/funkce-function_mc_funkce-function). A (real) function $f$ is a mapping from a non-empty subset $A \subset R$, called the **domain** $D(f)$, to $R$. The **range** $R(f)$ is the set of all values $f(A) = \{f(x): x \in A\}$. Key properties of functions were then introduced:
*   An [injective function (prostá)](https://felwiki.basta.one/en/Concepts/prost-injective-one-to-one_mc_prostá-injective-one-to-one) maps distinct inputs to distinct outputs.
*   A [surjective function (na)](https://felwiki.basta.one/en/Concepts/na-surjective-onto_mc_na-surjective-onto) means its range equals its codomain.
*   A [bijective function (vzájemně jednoznačná)](https://felwiki.basta.one/en/Concepts/vz-jemn-jednozna-n-bijection_mc_vzájemně-jednoznačná-bijection) is both injective and surjective.
The concept of an [inverse function](https://felwiki.basta.one/en/Concepts/inverzn-funkce-inverse-function_mc_inverzní-funkce-inverse-function) $f^{-1}$ was defined, existing if and only if the original function $f$ is injective. Its domain is the range of $f$, and vice versa, with its graph being symmetric to $f$'s graph across the line $y=x$.

Functions can also exhibit specific behaviors:
*   A [monotonic function](https://felwiki.basta.one/en/Concepts/monotonn-monotonic-function_mc_monotonní-monotonic-function) is one that is either strictly increasing, strictly decreasing, non-decreasing, or non-increasing. A strictly monotonic function is always injective, and its inverse is also monotonic.
*   An [even function](https://felwiki.basta.one/en/Concepts/sud-funkce-even-function_mc_sudá-funkce-even-function) satisfies $f(-x) = f(x)$ for all $x$ in its domain.
*   An [odd function](https://felwiki.basta.one/en/Concepts/odd-function_mc_odd-function) satisfies $f(-x) = -f(x)$.
*   A [periodic function](https://felwiki.basta.one/en/Concepts/periodic-function_mc_periodic-function) with period $p > 0$ satisfies $f(x+p) = f(x)$.

## Limits of Functions

A cornerstone of calculus, the [limit of a function](https://felwiki.basta.one/en/Concepts/limit-of-a-function_mc_limit-of-a-function), was rigorously defined. For a function $f$ defined in a punctured neighborhood of $a \in R$, it has a limit $b \in R$ if for every neighborhood $U$ of $b$, there exists a punctured neighborhood $P$ of $a$ such that $f(P) \subset U$. This is expressed as $\lim_{x \to a} f(x) = b$.

The lecture further introduced [one-sided limits](https://felwiki.basta.one/en/Concepts/jednostrann-limita-one-sided-limit_mc_jednostranná-limita-one-sided-limit) (from the left, $x \to a^-$, and from the right, $x \to a^+$). A crucial theorem states that a limit exists if and only if both one-sided limits exist and are equal. Several properties of limits were presented:
*   The [uniqueness theorem of limits](https://felwiki.basta.one/en/Concepts/v-ta-o-jednozna-nosti-uniqueness-theorem-of-limits_mc_věta-o-jednoznačnosti-uniqueness-theorem-of-limits) asserts that a function has at most one limit at any given point.
*   The [monotonicity theorem for limits](https://felwiki.basta.one/en/Concepts/v-ta-o-monotonii-limit-monotonicity-theorem-for-limits_mc_věta-o-monotonii-limit-monotonicity-theorem-for-limits) states that if $f(x) \le g(x)$ in a punctured neighborhood of $a$, then $\lim f(x) \le \lim g(x)$.
*   Functions with a finite limit are bounded in a punctured neighborhood.
*   The limit of a sum, difference, product, or quotient of functions is the sum, difference, product, or quotient of their limits, provided the operations are defined (including with infinite numbers).
*   The [Squeeze Theorem (o sevření)](https://felwiki.basta.one/en/Concepts/v-ta-o-sev-en-squeeze-theorem_mc_věta-o-sevření-squeeze-theorem) is a powerful tool: if $f(x) \le h(x) \le g(x)$ and $\lim f(x) = \lim g(x) = b$, then $\lim h(x) = b$.
*   A significant fundamental limit was given as:
    $$ \lim_{x \to 0} \frac{\sin x}{x} = 1 $$
The lecture also covered scenarios where limits involve infinity or do not exist, and the behavior of functions under composition of limits. For instance, if $\lim_{x \to a} f(x) = b$ and $\lim_{y \to b} g(y) = c$, then $\lim_{x \to a} (g \circ f)(x) = c$, provided certain conditions are met (e.g., $f(x) \ne b$ in a punctured neighborhood of $a$).

## Continuity of Functions

Building on the concept of limits, the lecture introduced [continuity of a function](https://felwiki.basta.one/en/Concepts/spojit-funkce-continuous-function_mc_spojitá-funkce-continuous-function). A function $f$ is continuous at a point $a \in D(f)$ if $\lim_{x \to a} f(x) = f(a)$. A function is considered continuous if it is continuous at every point in its domain.

Key properties of continuous functions include:
*   Sums, differences, products, and quotients (where the denominator is non-zero) of continuous functions are continuous.
*   A function continuous at a point is bounded in its neighborhood.
*   If $f$ is continuous at $a$ and $f(a) > 0$, then $f(x) > 0$ in a neighborhood of $a$.
*   The composition of continuous functions is continuous.
Important theorems regarding continuous functions on intervals were highlighted:
*   **Weierstrass Extreme Value Theorem:** A continuous function on a closed interval attains its maximum and minimum values.
*   The [Intermediate Value Theorem (o mezihodnotě)](https://felwiki.basta.one/en/Concepts/intermediate-value-theorem-o-mezihodnot_mc_intermediate-value-theorem-o-mezihodnotě): If a function is continuous on an interval and takes on values $m$ and $M$, then it takes on all values between $m$ and $M$.
A direct consequence of these theorems is that an inverse function to a strictly monotonic function on an interval is continuous.

## Derivatives and Differentiation Rules

The lecture then moved to the fundamental concept of the [derivative of a function](https://felwiki.basta.one/en/Concepts/derivative-of-a-function_mc_derivative-of-a-function). The derivative of $f$ at point $a$, denoted $f'(a)$ or $\frac{df}{dx}(a)$, is defined as:
$$ f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h} = \lim_{x \to a} \frac{f(x) - f(a)}{x-a} $$
One-sided derivatives (from the left and right) were also mentioned. A crucial relationship between differentiability and continuity was established: the [differentiability implies continuity theorem](https://felwiki.basta.one/en/Concepts/differentiability-implies-continuity-theorem_mc_differentiability-implies-continuity-theorem) states that if a function has a finite derivative at a point, it must be continuous at that point.

Basic differentiation rules introduced were:
*   The derivative of a constant $c$ is zero: $(c)' = 0$.
*   The power rule: $(x^a)' = ax^{a-1}$.
*   The derivative of the exponential function: $(e^x)' = e^x$.
*   Derivatives of trigonometric functions: $(\sin x)' = \cos x$ and $(\cos x)' = -\sin x$.

The lecture also covered rules for combinations of functions:
*   **Sum/Difference Rule:** $(f \pm g)'(a) = f'(a) \pm g'(a)$.
*   **Product Rule:** $(fg)'(a) = f'(a)g(a) + f(a)g'(a)$.
*   **Quotient Rule:** $(f/g)'(a) = \frac{f'(a)g(a) - f(a)g'(a)}{g(a)^2}$, for $g(a) \ne 0$.
*   The [Chain Rule](https://felwiki.basta.one/en/Concepts/chain-rule_mc_chain-rule) for composite functions: $(g \circ f)'(a) = g'(f(a)) \cdot f'(a)$.
*   The derivative of an inverse function: if $f$ is continuous and strictly monotonic on an interval $I$, and $f'(a) \ne 0$, then $(f^{-1})'(f(a)) = \frac{1}{f'(a)}$.

## Mean Value Theorems and L'Hôpital's Rule

The lecture concluded with fundamental theorems of differential calculus that relate the derivative to the function's behavior over an interval:
*   [Rolle's Theorem](https://felwiki.basta.one/en/Concepts/rolle-s-theorem_mc_rolles-theorem): If $f$ is continuous on $[a,b]$, differentiable on $(a,b)$, and $f(a) = f(b)$, then there exists a $c \in (a,b)$ such that $f'(c) = 0$.
*   [Lagrange's Mean Value Theorem (o přírůstku funkce)](https://felwiki.basta.one/en/Concepts/lagrange-s-mean-value-theorem-o-p-r-stku-funkce_mc_lagranges-mean-value-theorem-o-přírůstku-funkce): If $f$ is continuous on $[a,b]$ and differentiable on $(a,b)$, there exists a $c \in (a,b)$ such that $f(b) - f(a) = f'(c) \cdot (b-a)$.
*   [Cauchy's Mean Value Theorem](https://felwiki.basta.one/en/Concepts/cauchyho-v-ta-cauchy-s-mean-value-theorem_mc_cauchyho-věta-cauchys-mean-value-theorem): If $f$ and $g$ are continuous on $[a,b]$, differentiable on $(a,b)$, and $g'(x) \ne 0$ on $(a,b)$, then there exists $c \in (a,b)$ such that $\frac{f(b)-f(a)}{g(b)-g(a)} = \frac{f'(c)}{g'(c)}$.
*   [L'Hôpital's Rule](https://felwiki.basta.one/en/Concepts/l-hospitalovo-pravidlo-l-h-pital-s-rule_mc_lhospitalovo-pravidlo-lhôpitals-rule) for evaluating indeterminate forms ($0/0$ or $\pm\infty/\pm\infty$): If $\lim_{x \to a} f(x) = \lim_{x \to a} g(x) = 0$ (or $\pm\infty$), and $\lim_{x \to a} \frac{f'(x)}{g'(x)} = b$ exists, then $\lim_{x \to a} \frac{f(x)}{g(x)} = b$.

This lecture serves as a comprehensive introduction to the essential building blocks of calculus, laying the groundwork for more advanced topics in mathematical analysis.

### Keywords
Calculus, Real Analysis, Functions, Limits, Derivatives