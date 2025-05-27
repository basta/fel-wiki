# Bounds (Supremum & Infimum)

## Summary
An upper bound (horní závora) for a set M is $z$ if $M \leq z$. A lower bound (dolní závora) is $z$ if $z \leq M$. Supremum (sup M) is the least upper bound, and Infimum (inf M) is the greatest lower bound. Every set of real numbers has a unique supremum and infimum.

## Detailed Explanation
The concepts of bounds, supremum, and infimum are fundamental to real analysis, providing a precise way to describe the "edge" or "limit" of a set of real numbers, even if those edges are not contained within the set itself.

**Definition:**
*   **From calculus-intro-basic-concepts-lect01:** "An upper bound (horní závora) for a set M is z if M ≤ z. A lower bound (dolní závora) is z if z ≤ M. Supremum (sup M) is the least upper bound, and Infimum (inf M) is the greatest lower bound. Every set of real numbers has a unique supremum and infimum."

Let $S$ be a non-empty subset of real numbers ($\mathbb{R}$). 

*   **Upper Bound:** A real number $U$ is an upper bound of $S$ if for every $x \in S$, $x \leq U$.
*   **Lower Bound:** A real number $L$ is a lower bound of $S$ if for every $x \in S$, $L \leq x$.
*   **Supremum (Least Upper Bound):** The supremum of $S$, denoted $\sup(S)$, is the smallest number among all upper bounds of $S$. If a set has no upper bound (e.g., $(-\infty, \infty)$), its supremum is considered $+\infty$ in the extended real number system.
*   **Infimum (Greatest Lower Bound):** The infimum of $S$, denoted $\inf(S)$, is the largest number among all lower bounds of $S$. If a set has no lower bound, its infimum is considered $-\infty$.

A crucial property of the real numbers is the **Completeness Axiom**, which states that every non-empty set of real numbers that is bounded above has a supremum in $\mathbb{R}$, and every non-empty set of real numbers that is bounded below has an infimum in $\mathbb{R}$. This guarantees the existence and uniqueness of the supremum and infimum for bounded sets.

## Importance/Relevance
This is a highly important concept (Importance Score: 0.9). Supremum and infimum are crucial for defining convergence of sequences, continuity of functions, and for establishing many key theorems in real analysis, such as the Intermediate Value Theorem and the Extreme Value Theorem. They allow for a rigorous understanding of the "least" or "greatest" values associated with sets, even when those values are not explicitly part of the set (e.g., for open intervals).

## Connections
This concept appears in the lecture:
*   "Introduction to Real Functions and Fundamental Calculus Concepts" (calculus-intro-basic-concepts-lect01)

## Category
Core Principle