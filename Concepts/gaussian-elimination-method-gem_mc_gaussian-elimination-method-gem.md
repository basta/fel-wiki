# Gaussian Elimination Method (GEM)

## Summary
The Gaussian Elimination Method (GEM) is a universal and systematic method primarily used for solving systems of linear equations. It's important to note that while powerful, it can be numerically unstable when applied to large systems over real or complex numbers.

## Detailed Explanation
### Definition
According to the lecture "GEM a soustavy lineárních rovnic, část 2" (ID: 06B-2024-GEM-souostavy-cast2):
> A universal and systematic method for solving systems of linear equations. It can be numerically unstable when applied to large systems over real or complex numbers.

GEM involves a series of elementary row operations (swapping rows, multiplying a row by a non-zero scalar, and adding a multiple of one row to another) to transform the augmented matrix of a system of linear equations into an equivalent row echelon form (or reduced row echelon form). From this form, the solution to the system can be easily obtained through back-substitution. While highly effective, its numerical stability can be a concern for very large systems or systems with ill-conditioned matrices, potentially leading to significant rounding errors.

## Importance/Relevance
This concept is highly relevant and fundamental in linear algebra as it provides a systematic and widely applicable algorithm for solving systems of linear equations, which appear in virtually every scientific and engineering discipline.

## Connections
### Appears In
*   [GEM a soustavy lineárních rovnic, část 2](06B-2024-GEM-souostavy-cast2)

### Category
Algorithm