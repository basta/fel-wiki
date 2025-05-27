# Gaussova eliminační metoda (GEM)

## Summary
A universal and systematic method for solving systems of linear equations by applying a sequence of elementary row operations to transform the augmented matrix into an upper block (row echelon) form.

## Detailed Explanation
The Gaussian Elimination Method, often abbreviated as GEM, is a cornerstone algorithm in linear algebra for solving systems of linear equations. Its systematic nature ensures that it can be applied to any system, regardless of its size or complexity, to determine if solutions exist and, if so, what they are. The core idea is to transform the [augmented matrix](#mc_rozšířená-matice-soustavy-augmented-matrix) of the system into an [upper block (row echelon) form](#mc_horní-blokový-tvar-matice-upper-block-form-matrix) using a series of [elementary row operations](#mc_řádkové-elementární-úpravy-elementary-row-operations).

*   **Definition:** A universal and systematic method for solving systems of linear equations by applying a sequence of elementary row operations to transform the augmented matrix into an upper block (row echelon) form. (Source: 06A-2024-GEM-LinearSystems-Part1)

Once the matrix is in upper block form, the system can be easily solved using back-substitution. The process involves creating zeros below the main diagonal using pivots, thereby isolating variables.

## Importance
This concept is of *critical importance* (score: 1.0) as it is a fundamental algorithm for solving linear systems, widely used in mathematics, engineering, computer science, and various scientific fields. It forms the basis for many other numerical methods and theoretical results in linear algebra.

## Connections
This concept appears in the following lectures:
*   [GEM a soustavy lineárních rovnic, část 1](06A-2024-GEM-LinearSystems-Part1)

## Category
Algorithm