# dolní závora (Lower Bound)

## Summary
For a set $M$ of real numbers, a number $z$ is a lower bound if all elements in $M$ are greater than or equal to $z$ (i.e., for all $x \in M$, $z \le x$).

## Detailed Explanation
The concept of a lower bound is symmetric to that of an upper bound and is equally fundamental in real analysis and set theory, especially for describing sets that are "bounded" from below.

The provided definition states:
"For a set $M$, a number $z$ is a lower bound if all elements in $M$ are greater than or equal to $z$ ($z \le M$)." (Source: Fundamentals of Mathematical Analysis)

In more formal terms, if $M$ is a non-empty subset of the real numbers $\mathbb{R}$, a number $z \in \mathbb{R}$ is called a **lower bound** of $M$ if for every element $x$ in $M$, it holds that $z \le x$.

**Example:**
Consider the set $M = \{1, 2, 3\}$.
*   $1$ is a lower bound because $1 \le 1$, $1 \le 2$, $1 \le 3$.
*   $0$ is also a lower bound because $0 \le 1$, $0 \le 2$, $0 \le 3$.
*   Any number less than or equal to $1$ is a lower bound for this set.

Consider the interval $I = (0, 5)$.
*   $0$ is a lower bound because for any $x \in (0, 5)$, $x > 0$, which implies $0 \le x$.
*   $-5$ is also a lower bound.
Any number less than or equal to $0$ is a lower bound for this set.

If a set has a lower bound, it is said to be **bounded below**. Similar to upper bounds, a set can have infinitely many lower bounds if it has at least one. The largest of all lower bounds is called the **greatest lower bound** or **infimum**.

## Importance/Relevance
Lower bounds are highly important (score: 0.7) for defining bounded sets, understanding properties of real numbers, and are crucial for the definition of infimum, which is a counterpart to supremum and equally vital in the completeness axiom of real numbers and advanced mathematical analysis.

## Connections
This concept appears in the lecture:
*   Fundamentals of Mathematical Analysis

## Category
Set Property