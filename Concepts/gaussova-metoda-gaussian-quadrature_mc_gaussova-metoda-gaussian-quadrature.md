# Gaussova metoda (Gaussian Quadrature)

## Summary
Gaussian Quadrature is a highly efficient numerical integration method distinguished by its optimal selection of nodes (points where the function is evaluated) and weights. This optimal choice provides a significantly higher order of approximation, specifically $2 \times (\text{number of nodes})$, compared to methods using equally spaced points.

## Detailed Explanation
Unlike methods like Newton-Cotes which rely on equidistant points, Gaussian Quadrature strategically places its nodes and assigns corresponding weights to achieve maximum accuracy for a given number of function evaluations. This makes it particularly effective for approximating definite integrals.

### Definition
*   **From Lecture "Mathematical Analysis: Integrals, Series, and Numerical Methods" (ID: lec_0a0dc037-8067-470a-8948-277889b1ab2d):**
    A numerical integration method characterized by optimal choice of nodes and weights, providing a higher order of approximation ($2 \times \text{number of nodes}$).

## Importance/Relevance
With an overall importance score of 0.8, Gaussian Quadrature is a highly significant method in numerical analysis, prized for its exceptional accuracy and efficiency in approximating integrals, especially when precise results are needed with a limited number of function evaluations.

## Connections
### Appears In
*   Mathematical Analysis: Integrals, Series, and Numerical Methods (Lecture ID: lec_0a0dc037-8067-470a-8948-277889b1ab2d)

## Category
Numerical Integration Method