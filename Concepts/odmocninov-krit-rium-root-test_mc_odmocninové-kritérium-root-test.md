# Odmocninové kritérium (Root test)

## Summary
The Root Test is a convergence test similar to the Ratio Test, where the condition for convergence or divergence is based on the limit of the $k$-th root of the absolute value of the terms, i.e., $\lim_{k\to\infty} \sqrt[k]{|a_k|}$.

## Detailed Explanation
The Root Test is particularly useful for series where the terms involve powers of $k$.
*   **Definition:** A convergence test similar to the ratio test, where the condition is based on $\sqrt[k]{|a_k|}$.
    *   Let $L = \lim_{k\to\infty} \sqrt[k]{|a_k|}$.
        *   If $L < 1$, the series $\sum a_k$ converges absolutely.
        *   If $L > 1$ or $L = \infty$, the series $\sum a_k$ diverges.
        *   If $L = 1$, the test is inconclusive, and other tests must be used.
    *   *Source:* Mathematical Analysis: Integrals, Series, and Numerical Methods (lec_0a0dc037-8067-470a-8948-277889b1ab2d)

This test is especially effective for series like $\sum (f(k))^k$ because the $k$-th root simplifies the expression significantly, making the limit easier to evaluate.

## Importance/Relevance
This concept is of **high importance** (score: 0.7) as it provides another powerful method for testing the convergence of series, particularly when the terms are structured as powers of $k$. It is often interchangeable with the Ratio Test, but one may be easier to apply than the other depending on the series structure.

## Connections
This concept appears in the lecture:
*   Mathematical Analysis: Integrals, Series, and Numerical Methods

## Category
Convergence Criterion