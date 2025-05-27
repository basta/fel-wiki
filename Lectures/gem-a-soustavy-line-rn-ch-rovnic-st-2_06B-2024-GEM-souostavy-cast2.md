# GEM a soustavy lineárních rovnic, část 2
## Lineární algebra - Lecture 2
Presented by Jiří Velebil.

This lecture, the second part focusing on the Gaussian Elimination Method (GEM) and systems of linear equations, expanded upon the foundational concepts introduced previously. The primary objective was to demonstrate the versatility of GEM in solving more complex problems, particularly linear matrix equations, and to tackle the inverse problem of constructing a linear system from a given solution set. The discussion also included important practical considerations regarding the numerical stability of GEM. The content covered can be found in chapters 6 and 7.1 of "Abstraktní a konkrétní lineární algebra."

### Solving Linear Matrix Equations

The lecture began by addressing **linear matrix equations**, which are equations where the unknown is a matrix `X` appearing in its first power. A universal approach to solving such equations, like `Ra * X = X * Ra`, involves converting them into a system of linear equations.

Consider the example of finding all matrices `X` that commute with a rotation matrix `Ra: R² → R²`. The condition is `Ra * X = X * Ra`. By performing a dimensional check, it's clear `X` must also be a 2x2 matrix, `X = ((X11, X12), (X21, X22))`. This matrix equation can be rewritten as `Ra * X - X * Ra = O2,2`, leading to a system of four linear equations.

The solution to this system depends on the rotation angle $\alpha$.
*   For $\sin \alpha = 0$ (i.e., $\alpha = 0$ or $\alpha = \pi$), the system simplifies significantly. In this case, any 2x2 matrix `X` will commute with `Ra`. This means any transformation of the plane is interchangeable with a rotation by 0 or $\pi$.
*   For $\sin \alpha \neq 0$, the system leads to solutions of the form:
    $$X = a \cdot \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} + b \cdot \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$$
    where `a` and `b` are arbitrary real numbers. Geometrically, these matrices represent transformations that commute with rotations where the angle is not 0 or $\pi$.

While this method of expanding a matrix equation into a large system of equations and then applying [Gaussian Elimination Method (GEM)](https://felwiki.basta.one/en/Concepts/gaussian-elimination-method-gem) is universal, it can be computationally intensive.

#### Converting $A \cdot X = B$ into Multiple Systems

A more specialized and often more efficient method for solving matrix equations of the form `A * X = B` was then presented. This method, termed [Matrix Equation Conversion](https://felwiki.basta.one/en/Concepts/matrix-equation-conversion), involves breaking down the single matrix equation into multiple individual systems of linear equations. If `B` is composed of columns $(b_1, b_2, \dots, b_p)$, then the equation `A * X = B` is equivalent to solving `p` separate linear systems: `A * x = b_i` for each column $b_i$ of $B$.

The overall matrix equation `A * X = B` has a solution if and only if every one of these individual systems `A * x = b_i` has a solution. If solutions `x_1, x_2, \dots, x_p` are found for each system, then assembling them as columns yields the solution matrix `X = (x_1 \ x_2 \ \dots \ x_p)`. These systems can be solved simultaneously by constructing an augmented matrix `(A | B)` and applying row operations.

For instance, to solve $\begin{pmatrix} 1 & 2 \\ 1 & -3 \end{pmatrix} \cdot X = \begin{pmatrix} 2 & 1 \\ 1 & 2 \end{pmatrix}$ over $\mathbb{R}$:
This requires solving two individual systems, which can be done simultaneously using the augmented matrix:
$$\begin{pmatrix} 1 & 2 & | & 2 & 1 \\ 1 & -3 & | & 1 & 2 \end{pmatrix} \sim \dots \sim \begin{pmatrix} 1 & 2 & | & 2 & 1 \\ 0 & -5 & | & -1 & 1 \end{pmatrix}$$
Both resulting systems, `(1 2 | 2)` and `(1 2 | 1)` with `(-5 | -1)` and `(-5 | 1)` respectively, have solutions according to [Frobenius' Theorem](https://felwiki.basta.one/en/Concepts/frobeniova-v-ta-frobenius-theorem). The general solution `X` is formed by combining the solutions for each column.

For the special case where `A` is a [regular matrix](https://felwiki.basta.one/en/Concepts/regul-rn-matice-regular-matrix) (i.e., invertible), the equation `A * X = B` has a unique solution given by `X = A⁻¹ * B`. This solution can be efficiently found using [Gauss-Jordan Elimination](https://felwiki.basta.one/en/Concepts/gauss-jordan-elimination), where row operations are performed until the left side of the augmented matrix `(A | B)` becomes the identity matrix `Eⁿ`, leaving `(Eⁿ | A⁻¹ * B)`. This method is also used to find the inverse of a matrix `A` by setting up `(A | Eⁿ)` and transforming it to `(Eⁿ | A⁻¹)`.

### Finding a Linear System from its Solution (The Inverse Problem)

A significant part of the lecture focused on the **inverse problem**: given a set of solutions, how does one find the corresponding linear system `A * x = b`? The general solution to a linear system is often expressed as an [Affine Subspace](https://felwiki.basta.one/en/Concepts/affine-subspace_mc_affine-subspace) of the form `p + span(x₁, ..., xᴅ)`, where `p` is a [particular solution](https://felwiki.basta.one/en/Concepts/partikul-rn-e-en-particular-solution) and `span(x₁, ..., xᴅ)` represents the solution space of the associated [homogeneous system](https://felwiki.basta.one/en/Concepts/homogenn-soustava-homogeneous-system) `A * x = o`. The vectors `x₁, ..., xᴅ` are [linearly independent](https://felwiki.basta.one/en/Concepts/line-rn-nez-vislost_mc_lineární-nezávislost) and form a [Fundamental System (of homogeneous equations)](https://felwiki.basta.one/en/Concepts/fundamental-system-of-homogeneous-equations) for `A * x = o`.

The process for [Finding System from Solution (Inverse Problem)](https://felwiki.basta.one/en/Concepts/finding-system-from-solution-inverse-problem) involves two main steps:
1.  **Finding Matrix A:** The vectors `x₁, ..., xᴅ` must satisfy `A * xᵢ = o`. This means each `xᵢ` is in the null space (kernel) of `A`. If we denote the rows of `A` as `a_j`, then `a_j * xᵢ = 0` for all `i, j`. This is equivalent to finding the rows of `A` from the homogeneous system `Xᵀ * a = o`, where `X` is the matrix whose columns are `x₁, ..., xᴅ`. The rows of `A` will form a basis for the null space of `Xᵀ`.
2.  **Finding Vector b:** Once `A` is determined, the vector `b` can be found by substituting the particular solution `p` into the equation `A * p = b`.

**Example 1:** Find a system `A * x = b` whose solution is `((3),(2),(6)) + span(((1),(2),(0)), ((2),(0),(4)))` in $\mathbb{R}^3$.
Here, `p = ((3),(2),(6))` and the spanning vectors are `x₁ = ((1),(2),(0))` and `x₂ = ((2),(0),(4))`.
*   To find `A = (a₁ a₂ a₃)`, we set up the homogeneous system for `a = ((a1),(a2),(a3))`, where the rows are the transposes of `x₁` and `x₂`:
    $$\begin{pmatrix} 2 & 0 & 4 & | & 0 \\ 1 & 2 & 0 & | & 0 \end{pmatrix}$$
    Solving this, we find a fundamental system for `a` is `((2),(-1),(-1))`. Thus, `A = (2 -1 -1)`.
*   To find `b`, we substitute `p` into `A * p = b`:
    $$b = (2 \ -1 \ -1) \cdot \begin{pmatrix} 3 \\ 2 \\ 6 \end{pmatrix} = 2 \cdot 3 + (-1) \cdot 2 + (-1) \cdot 6 = 6 - 2 - 6 = -2$$
The resulting system is `(2 -1 -1 | -2)`, or `2x - y - z = -2`.

**Example 2:** Find a system `A * x = b` for the 3-dimensional [affine subspace](https://felwiki.basta.one/en/Concepts/affine-subspace_mc_affine-subspace) in $\mathbb{R}^5$: `((1),(1),(-2),(0),(2)) + span(((2),(1),(1),(0),(0)), ((1),(2),(0),(1),(0)), ((-1),(0),(1),(0),(1)))`.
Here `p = ((1),(1),(-2),(0),(2))` and the three spanning vectors form `X`. We construct `Xᵀ` and solve `Xᵀ * a = o`. The fundamental system for `a` gives the rows of `A`. After scaling to remove fractions, `A = ((-2,-1,5,4,0), (2,-1,-3,0,4))`. Then, `b` is computed as `A * p = ((-13),(15))`. The final system is:
$$\begin{pmatrix} -2 & -1 & 5 & 4 & 0 & | & -13 \\ 2 & -1 & -3 & 0 & 4 & | & 15 \end{pmatrix}$$

### Concluding Remarks on GEM

The lecture concluded with important remarks on the practical application of [Gaussian Elimination Method (GEM)](https://felwiki.basta.one/en/Concepts/gaussian-elimination-method-gem):
*   While GEM is a universal method for solving linear systems, it can be **numerically unstable** for large systems over real or complex numbers. This means small rounding errors during calculations can lead to large inaccuracies in the final solution.
*   For large-scale practical problems, iterative methods like the [Iterative Gauss-Seidel Method](https://felwiki.basta.one/en/Concepts/iterative-gauss-seidel-method) are often preferred due to their better [numerical stability](https://felwiki.basta.one/en/Concepts/numerical-stability). These advanced methods typically fall outside the scope of a standard linear algebra course.
*   When using GEM to solve systems involving parameters, extreme caution must be exercised during elementary row operations to avoid errors based on parameter values (e.g., division by zero).
*   Future lectures will delve into other solution methods for square matrices, including a combination of GEM and [Cramer's Rule](https://felwiki.basta.one/en/Concepts/cramer-s-rule_mc_cramers-rule).
*   For those interested in a deeper geometric understanding, GEM can also be viewed through the lens of Householder reflections, particularly in real vector spaces.

### Keywords
Linear Algebra, Gaussian Elimination, Matrix Equations, Affine Subspaces, System of Linear Equations