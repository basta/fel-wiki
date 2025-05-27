# Fundamentals of Mathematical Analysis

This lecture provides a comprehensive overview of fundamental concepts in mathematical analysis, laying the groundwork for understanding advanced calculus. It delves into the properties of functions, sequences, and the basic principles of both differential and integral calculus, concluding with essential theorems that underpin the field.

The lecture begins by establishing the definition of higher-order [derivatives of a function](https://felwiki.basta.one/en/Concepts/derivace-f-du-n-n-t-derivace). The zero-th derivative, $f^{(0)}$, is simply the function $f$ itself, while the $n$-th derivative, $f^{(n)}$, is recursively defined as the first derivative of the $(n-1)$-th derivative, i.e., $f^{(n)} = (f^{(n-1)})'$. This sets the stage for approximating functions through polynomial series.

### Differential Calculus: Taylor Series, Monotonicity, and Extrema

A core principle introduced is **Taylor's Theorem**, which allows for the approximation of a function by a polynomial. The theorem states that if a function $f$ has continuous derivatives up to order $n \ge 0$ on an interval $(a, x)$, and the $(n+1)$-th derivative exists at every point in $(a, x)$, then there exists a point $c \in (a, x)$ such that the function $f(x)$ can be expressed as:

$$f(x)= f(a)+ \frac{f'(a)}{1!} (x−a)+…+ \frac{f^{(n)}(a)}{n!} (x−a)^n + \frac{f^{(n+1)}(c)}{(n+1)!} (x-a)^{n+1}$$

Here, the first part of the expression represents the [Taylor polynomial](https://felwiki.basta.one/en/Concepts/taylor-v-polynom-f-v-a-du-n-t_n-x) of $f$ at point $a$ of order $n$, denoted as $T_n(x)$. The final term, $\frac{f^{(n+1)}(c)}{(n+1)!} (x-a)^{n+1}$, is the [Lagrange form of the remainder](https://felwiki.basta.one/en/Concepts/zbytek-v-lagrangeov-tvaru), which quantifies the error of the approximation. Visual examples, such as the Taylor polynomial approximations of sine and cosine functions, underscore the utility of this theorem.

The lecture then transitions to the concept of [monotonicity of a function](https://felwiki.basta.one/en/Concepts/monotonie-funkce), linking it directly to the sign of the first derivative. A continuous function $f$ on an interval $I$ is increasing if $f'(x) > 0$ within $I$, decreasing if $f'(x) < 0$, non-decreasing if $f'(x) \ge 0$, and non-increasing if $f'(x) \le 0$. A related assertion highlights that if $f'(a) > 0$, there exists a neighborhood around $a$ where the function behaves monotonically increasing.

Following this, the lecture defines [local extrema](https://felwiki.basta.one/en/Concepts/lok-ln-extr-m). A function $f$ has a [local minimum](https://felwiki.basta.one/en/Concepts/lok-ln-minimum-maximum) at point $a$ if $f(x) \ge f(a)$ for all $x$ in some punctured neighborhood of $a$, and a [local maximum](https://felwiki.basta.one/en/Concepts/lok-ln-minimum-maximum) if $f(x) \le f(a)$. If $f$ has a local extremum at $a$, then either $f'(a) = 0$ (meaning $a$ is a [stationary point](https://felwiki.basta.one/en/Concepts/stacion-rn-bod)) or $f'(a)$ does not exist. The second derivative test provides a more definitive criterion for classifying stationary points: if $f'(a)=0$ and $f''(a) > 0$, $f$ has a sharp local minimum at $a$; if $f''(a) < 0$, it has a sharp local maximum. Importantly, for a continuous function on a closed interval, global maxima and minima are attained either at local extrema or at the interval's endpoints.

### Function Properties: Convexity, Concavity, Inflection Points, and Asymptotes

The lecture further explores the shape of a function's graph by introducing the concepts of [convexity](https://felwiki.basta.one/en/Concepts/konvexn-funkce) and [concavity](https://felwiki.basta.one/en/Concepts/konk-vn-funkce). A function $f$ is defined as convex on an interval $I$ if for any $x < y < z$ in $I$, the slope of the secant line from $(x, f(x))$ to $(y, f(y))$ is less than or equal to the slope of the secant line from $(y, f(y))$ to $(z, f(z))$, i.e.:

$$\frac{f(y)-f(x)}{y-x} \le \frac{f(z)-f(y)}{z-y}$$

A direct link to the second derivative is established: if $f''(x) \ge 0$ inside $I$, $f$ is convex on $I$; if $f''(x) \le 0$, it is concave. Strictly convex/concave functions correspond to strict inequalities. A point where a function changes its convexity/concavity is called an [inflection point](https://felwiki.basta.one/en/Concepts/inflexn-bod). For a point $[a, f(a)]$ to be an inflection point, $f$ must be continuous at $a$, $f'(a)$ must exist (possibly improper), and $f$ must change from strictly convex to strictly concave (or vice-versa) in a one-sided neighborhood of $a$. If $f''(a)=0$ and $f'''(a) \neq 0$, then $f$ has an inflection point at $a$.

Another crucial feature of function graphs is an [asymptote](https://felwiki.basta.one/en/Concepts/asymptota-grafu-funkce). A vertical asymptote occurs at $x=a$ if $f$ has at least one improper one-sided limit at $a$. For oblique asymptotes of the form $y=px+q$ as $x$ approaches $\pm\infty$, the coefficients $p$ and $q$ are determined by the limits:

$$p = \lim_{x\to a} \frac{f(x)}{x}$$
$$q = \lim_{x\to a} (f(x)-px)$$

Practical examples illustrate these concepts, such as analyzing $f(x) = x^3 - 3x^2 + 3|x|$ or $f(x) = x^2 / (x+1)^2$ to identify their shapes, extrema, and asymptotes.

### Fundamental Theorems of Analysis

The lecture highlights several foundational theorems:
*   The **Principle of Nested Intervals** states that if $I_1 \supset I_2 \supset \dots$ are a sequence of closed intervals, their intersection is non-empty. Furthermore, if the lengths of these intervals tend to zero, their intersection is a single point.
*   The **Weierstrass Theorem** asserts that a continuous function on a closed interval attains both its maximum and minimum values within that interval. This complements the discussion on finding extrema.
*   The **Intermediate Value Theorem** ([o mezihodnotě](https://felwiki.basta.one/en/Concepts/intermediate-value-theorem-o-mezihodnot_mc_intermediate-value-theorem-o-mezihodnotě)) states that if a function $f$ is continuous on an interval and takes on values $m < M$ within that interval, then it must also take on all values between $m$ and $M$.

### Sequences and Set Theory

The discussion shifts to the study of [sequences of real numbers](https://felwiki.basta.one/en/Concepts/posloupnost-re-ln-ch-sel), defined as a mapping from natural numbers to real numbers. A sequence $(a_n)_{n=1}^\infty$ is said to have a limit $a \in \mathbb{R}$ (i.e., $\lim_{n\to\infty} a_n = a$) if for every neighborhood $U$ of $a$, there exists an $n_0 \in \mathbb{N}$ such that for all $n > n_0$, $a_n \in U$. A sequence with a finite limit is termed a [convergent sequence](https://felwiki.basta.one/en/Concepts/konvergentn-posloupnost), and convergent sequences are always bounded. The lecture emphasizes the relationship between function limits and sequence limits: $\lim_{x\to a} f(x) = b$ if and only if $\lim_{n\to\infty} f(a_n) = b$ for every sequence $(a_n)_{n=1}^\infty$ in the domain of $f$ (excluding $a$) that converges to $a$.

A [subsequence](https://felwiki.basta.one/en/Concepts/vybran-posloupnost-podposloupnost) is formed by selecting terms from the original sequence while maintaining their relative order. An [accumulation point](https://felwiki.basta.one/en/Concepts/hromadn-hodnota-posloupnosti) (or limit point) of a sequence is a number $a \in \mathbb{R}$ such that every neighborhood of $a$ contains infinitely many terms of the sequence. This is equivalent to $a$ being the limit of some subsequence. Every sequence has at least one accumulation point, and every bounded sequence has a finite accumulation point. The supremum and infimum of the set of accumulation points are themselves accumulation points, known as the [limes superior](https://felwiki.basta.one/en/Concepts/limes-superior) and [limes inferior](https://felwiki.basta.one/en/Concepts/limes-inferior), respectively. Several equivalent conditions for a sequence to have a limit are presented: having a single accumulation point, having equal limes superior and limes inferior, or every subsequence having the same limit.

Briefly, the lecture touches upon fundamental set theory concepts: [cardinality](https://felwiki.basta.one/en/Concepts/mohutnost-kardinalita) (or mohutnost), which compares the "size" of sets based on the existence of a bijection between them. Sets with the same cardinality as the natural numbers $\mathbb{N}$ are called [countable sets](https://felwiki.basta.one/en/Concepts/spo-etn-mno-iny). The lecture notes that rational numbers ($\mathbb{Q}$) are countable, while real numbers ($\mathbb{R}$) are uncountable.

### Introduction to Integral Calculus: Primitive Functions and Indefinite Integrals

The final segment of the lecture introduces the concept of a [primitive function](https://felwiki.basta.one/en/Concepts/primitivn-funkce) (also known as an antiderivative). A function $F$ is a primitive function of $f$ on an interval $I$ if $F' = f$ on $I$. It's noted that while some primitive functions, like for $e^{-x^2}$, exist, they may not be expressible using elementary functions. A significant theorem states that any continuous function on an interval possesses a primitive function. An example is given of a function $F(x) = x^2 \sin(1/x)$ for $x \neq 0$ and $F(0)=0$, which is continuous everywhere and serves as a primitive function.

The relationship between primitive functions is defined: if $F$ is a primitive function of $f$, then $F+c$ (for any constant $c \in \mathbb{R}$) is also a primitive function. Conversely, if $F_1$ and $F_2$ are both primitive functions of $f$ on an interval, then their difference $F_1 - F_2$ must be a constant. This leads to the definition of the [indefinite integral](https://felwiki.basta.one/en/Concepts/neur-it-integr-l) of $f$ on $I$ as the set of all primitive functions of $f$ on $I$.

### Keywords
Differential Calculus, Integral Calculus, Sequences and Series, Functions, Mathematical Analysis