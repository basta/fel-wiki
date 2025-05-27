# Podílové kritérium (Ratio test)

## Summary
The Ratio Test is used for a series $\sum a_k$ where $a_k \neq 0$. If $\left|\frac{a_{k+1}}{a_k}\right| \leq q < 1$, the series converges absolutely. If $\left|\frac{a_{k+1}}{a_k}\right| \geq 1$, it does not converge. In its limit form: if $\lim_{k\to\infty} \left|\frac{a_{k+1}}{a_k}\right| < 1$, it converges absolutely; if $\lim_{k\to\infty} \left|\frac{a_{k+1}}{a_k}\right| > 1$, it does not converge.

## Detailed Explanation
The Ratio Test is a powerful tool for determining the convergence or divergence of series, especially those involving factorials or powers.
*   **Definition:** For a series $\sum a_k$ with $a_k \neq 0$:
    *   If there exists a $q < 1$ such that $\left|\frac{a_{k+1}}{a_k}\right| \leq q$ for all sufficiently large $k$, the series converges absolutely.
    *   If $\left|\frac{a_{k+1}}{a_k}\right| \geq 1$ for all sufficiently large $k$, the series does not converge (i.e., it diverges).
    *   **Limit Form:** Let $L = \lim_{k\to\infty} \left|\frac{a_{k+1}}{a_k}\right|$.
        *   If $L < 1$, the series $\sum a_k$ converges absolutely.
        *   If $L > 1$ or $L = \infty$, the series $\sum a_k$ diverges.
        *   If $L = 1$, the test is inconclusive, and other tests must be used.
    *   *Source:* Mathematical Analysis: Integrals, Series, and Numerical Methods (lec_0a0dc037-8067-470a-8948-277889b1ab2d)

This test is particularly effective for series whose terms contain products or powers, as the ratio often simplifies. It directly links to the concept of absolute convergence.

## Importance/Relevance
This concept is of **very high importance** (score: 0.9) in the study of series convergence. It is one of the most frequently used and versatile tests for determining absolute convergence or divergence of a series, especially for power series.

## Connections
This concept appears in the lecture:
*   Mathematical Analysis: Integrals, Series, and Numerical Methods

## Category
Convergence Criterion