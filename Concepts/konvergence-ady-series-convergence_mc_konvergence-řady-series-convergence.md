# Konvergence řady (Series Convergence)

## Summary
A series converges if the limit of its sequence of partial sums is a finite number (the sum).

## Detailed Explanation
An infinite numerical series $\sum_{k=1}^\infty a_k$ is said to **converge** if the sequence of its partial sums, $(s_n)_{n=1}^\infty$, approaches a finite limit as $n$ tends to infinity. If this limit exists and is a finite number $S$, then $S$ is called the sum of the series.

Mathematically, a series converges if:
$$ \lim_{n\to\infty} s_n = \lim_{n\to\infty} \sum_{k=1}^n a_k = S $$
where $S$ is a finite real number. If a series converges, its terms must eventually approach zero, i.e., $\lim_{k\to\infty} a_k = 0$. However, the converse is not always true (e.g., the harmonic series).

*Definition from lec-math-2023-001:*
"A series converges if the limit of its sequence of partial sums is a finite number (the sum)."

## Importance and Relevance
This concept is of **high importance** (score: 0.9) as it is central to the study of infinite series. Understanding convergence is critical for determining when a series can be assigned a finite sum, which has vast applications in areas like differential equations, Fourier analysis, and numerical methods.

## Connections
This concept appears in the lecture:
*   "Laplaceova transformace, Integrály, Řady a Numerické Metody" (lec-math-2023-001)

## Category
Series Property