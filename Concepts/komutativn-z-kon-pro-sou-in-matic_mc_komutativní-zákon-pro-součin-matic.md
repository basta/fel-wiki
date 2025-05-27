# Komutativní zákon (pro součin matic)

## Summary
Matrix multiplication generally does not satisfy the commutative law (B.A ≠ A.B), even if both products are defined.

## Detailed Explanation
### Definition
The **Commutative Law for Matrix Multiplication** states that, in general, matrix multiplication is not commutative. This means that for two matrices `B` and `A`, the product `B.A` is typically not equal to `A.B`, even in cases where both products are dimensionally defined and thus computable.

*   **Source:** 04B-2024-Algebra-Matic: "Matrix multiplication generally does not satisfy the commutative law (B.A ≠ A.B), even if both products are defined."

### Elaboration
This is a critical distinction between matrix algebra and scalar algebra. For scalar numbers, `a * b` always equals `b * a`. However, with matrices, the order of multiplication matters significantly. This non-commutative nature arises from the row-by-column multiplication process inherent to matrix products. While there are specific cases where `A.B = B.A` (e.g., identity matrix, inverse matrix, or certain diagonal matrices), these are exceptions rather than the rule. Understanding this property is essential to avoid common errors in matrix calculations.

## Importance/Relevance
With an `overallImportanceScore` of 0.8, the understanding that matrix multiplication *does not* generally satisfy the commutative law is an important concept. It highlights a fundamental difference from scalar arithmetic and is crucial for correctly applying matrix operations in various fields.

## Connections
This concept appears in the following lecture:
*   **Algebra matic** (04B-2024-Algebra-Matic)

## Category
Property