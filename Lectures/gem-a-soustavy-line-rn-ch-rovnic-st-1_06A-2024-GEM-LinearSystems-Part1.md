# GEM a soustavy lineárních rovnic, část 1
## Lineární algebra - Lecture 1

This lecture, delivered by Jiří Velebil, serves as the first part of a comprehensive introduction to Gaussian Elimination Method (GEM) and its application in solving systems of linear equations. It builds upon previous discussions of matrices as linear mappings and their algebraic properties, setting the stage for a systematic approach to finding solutions for various linear systems.

### Foundations of Linear Systems

The lecture began by reiterating the core representation of a system of linear equations: the matrix equation $A \mathbf{x} = \mathbf{b}$, where $A$ is the coefficient [matice](https://felwiki.basta.one/en/Concepts/matice_mc_matice), $\mathbf{x}$ is the vector of unknowns, and $\mathbf{b}$ is the right-hand side vector. This formulation concisely encodes a [soustava lineárních rovnic](https://felwiki.basta.one/en/Concepts/soustava-lineárních-rovnic_mc_soustava-lineárních-rovnic) over a field $F$. A key concept introduced is the [rozšířená matice soustavy (augmented matrix)](https://felwiki.basta.one/en/Concepts/rozšířená-matice-soustavy-augmented-matrix_mc_rozšířená-matice-soustavy-augmented-matrix), denoted as $(A | \mathbf{b})$, which combines the coefficient matrix and the constant vector. For instance, the system $2x_1 - 4x_2 + 4x_3 = 12$ and $2x_1 + x_3 = -42$ can be represented as the augmented matrix $\begin{pmatrix} 2 & -4 & 4 & | & 12 \\ 2 & 0 & 1 & | & -42 \end{pmatrix}$.

Two fundamental perspectives for understanding the solution of linear systems were highlighted:
1.  **Geometric Interpretation:** For systems over $\mathbb{R}$, a solution represents the intersection of geometric entities (e.g., two lines intersecting at a point, or planes intersecting in a line or point). For example, $x - y = 4$ and $2x + y = 5$ describe two lines intersecting at a single point.
2.  **Linear Combination of Columns:** The right-hand side vector $\mathbf{b}$ can be viewed as a [lineární kombinace](https://felwiki.basta.one/en/Concepts/line-rn-kombinace-linear-combination_mc_lineární-kombinace-linear-combination) of the columns of matrix $A$. The solutions are then the coefficients of this linear combination. This perspective is particularly advantageous because it highlights how systematically transforming the system into a "nicer" form (via [isomorfismus](https://felwiki.basta.one/en/Concepts/isomorfismus_mc_isomorfismus)) can easily reveal these coefficients.

### Gaussian Elimination Method (GEM)

The central theme of the lecture was the introduction of the [Gaussova eliminační metoda (GEM)](https://felwiki.basta.one/en/Concepts/gaussova-eliminační-metoda-gem_mc_gaussova-eliminační-metoda-gem). GEM is presented as a universal and systematic algorithm for solving systems of linear equations over any field $F$. Its core idea is to transform the augmented matrix into a simplified form using a finite sequence of elementary row operations.

A matrix is considered to be in [horní blokový tvar matice (upper block form)](https://felwiki.basta.one/en/Concepts/horní-blokový-tvar-matice-upper-block-form-matrix_mc_horní-blokový-tvar-matice-upper-block-form-matrix) if:
1.  All non-zero rows are above any rows consisting entirely of zeros.
2.  The first non-zero entry (called a [pivot](https://felwiki.basta.one/en/Concepts/pivot_mc_pivot)) of any non-zero row is always to the right of the pivot of the row above it. An example of a matrix in upper block form is:
    $$
    \begin{pmatrix}
    3 & -1 & 4 & 6 & 1 & 5 & 32 \\
    0 & 0 & 6 & 2 & 3 & -4 & -1 \\
    0 & 0 & 0 & 12 & 2 & 8 & 14 \\
    0 & 0 & 0 & 0 & 0 & 0 & 0 \\
    0 & 0 & 0 & 0 & 0 & 0 & 0
    \end{pmatrix}
    $$

The [řádkové elementární úpravy (elementary row operations)](https://felwiki.basta.one/en/Concepts/řádkové-elementární-úpravy-elementary-row-operations_mc_řádkové-elementární-úpravy-elementary-row-operations) are the building blocks of GEM. There are three types:
1.  **Adding a scalar multiple of one row to another:** This operation is equivalent to multiplying the matrix by an appropriate "elementary" isomorphism matrix $P$. For instance, adding 3 times the first row to the third row of $M = \begin{pmatrix} 2 & 3 & 5 & 8 \\ 4 & 1 & 7 & 3 \\ 5 & 2 & 6 & 4 \end{pmatrix}$ results in $P \cdot M = \begin{pmatrix} 2 & 3 & 5 & 8 \\ 4 & 1 & 7 & 3 \\ 11 & 11 & 21 & 28 \end{pmatrix}$ where $P = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 3 & 0 & 1 \end{pmatrix}$.
2.  **Swapping two rows:** Also achieved by multiplying by an elementary isomorphism matrix. Swapping the first and third rows of $M$ leads to $P \cdot M = \begin{pmatrix} 5 & 2 & 6 & 4 \\ 4 & 1 & 7 & 3 \\ 2 & 3 & 5 & 8 \end{pmatrix}$ with $P = \begin{pmatrix} 0 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 0 & 0 \end{pmatrix}$.
3.  **Multiplying a row by a non-zero scalar:** Similarly, this is an isomorphic transformation. Multiplying the second row of $M$ by -5 gives $P \cdot M = \begin{pmatrix} 2 & 3 & 5 & 8 \\ -20 & -5 & -35 & -15 \\ 5 & 2 & 6 & 4 \end{pmatrix}$ with $P = \begin{pmatrix} 1 & 0 & 0 \\ 0 & -5 & 0 \\ 0 & 0 & 1 \end{pmatrix}$.

These operations are crucial because they transform a system into an [ekvivalentní soustavy (equivalent system)](https://felwiki.basta.one/en/Concepts/ekvivalentní-soustavy-equivalent-systems_mc_ekvivalentní-soustavy-equivalent-systems), meaning the new system has the exact same set of solutions as the original. Each elementary row operation corresponds to applying an isomorphism, preserving the solution set.

### Matrix Properties: Rank and Defect

The lecture further explored the important properties of matrices that are revealed through GEM:
*   The [hodnost matice (rank of a matrix)](https://felwiki.basta.one/en/Concepts/hodnost-matice-rank-of-a-matrix_mc_hodnost-matice-rank-of-a-matrix) is defined as the maximum number of linearly independent row or column vectors. It is shown that the rank of a matrix $M$ is equal to the rank of its transpose ($rank(M) = rank(M^T)$). Furthermore, the rank of a matrix is equal to the number of non-zero rows in its upper block form after GEM.
*   The [defekt matice (defect of a matrix)](https://felwiki.basta.one/en/Concepts/defekt-matice-defect-of-a-matrix_mc_defekt-matice-defect-of-a-matrix) $d$ is defined as the number of columns in the matrix minus its rank. For a system with $s$ unknowns, the defect of matrix $A$ is $d = s - rank(A)$.

### Solvability of Linear Systems: Frobenius Theorem

A cornerstone result for determining whether a linear system has a solution is the [Frobeniova věta (Frobenius Theorem)](https://felwiki.basta.one/en/Concepts/frobeniova-věta-frobenius-theorem_mc_frobeniova-věta-frobenius-theorem). It states that a system $(A | \mathbf{b})$ has a solution if and only if the rank of the coefficient matrix $A$ is equal to the rank of the augmented matrix $(A | \mathbf{b})$. That is, $rank(A) = rank(A | \mathbf{b})$.

Moreover, if a solution exists, the theorem describes its structure: given any particular solution $\mathbf{p}$ such that $A \mathbf{p} = \mathbf{b}$, then any other solution $\mathbf{x}_0$ can be expressed as $\mathbf{x}_0 = \mathbf{p} + \mathbf{x}_h$, where $\mathbf{x}_h$ is a solution to the corresponding [homogenní soustava (homogeneous system)](https://felwiki.basta.one/en/Concepts/homogenní-soustava-homogeneous-system_mc_homogenní-soustava-homogeneous-system) $A \mathbf{x} = \mathbf{o}$. The set of all solutions can be written as $\mathbf{p} + ker(A)$, where $ker(A)$ is the kernel (or null space) of matrix $A$, which consists of all vectors $\mathbf{x}_h$ such that $A \mathbf{x}_h = \mathbf{o}$.

### Systematic Solution using GEM

The lecture then detailed how to systematically solve both homogeneous and non-homogeneous systems using GEM.

**Solving a Homogeneous System ($A \mathbf{x} = \mathbf{o}$):**
1.  Apply GEM to the augmented matrix $(A | \mathbf{o})$ to obtain its upper block form $(A' | \mathbf{o})$.
2.  Determine the rank of $A'$ (which equals $rank(A)$) by counting its non-zero rows.
3.  Calculate the defect $d = s - rank(A')$, which indicates the number of "free" variables. These free variables correspond to columns in $A'$ that do not contain a pivot.
4.  To find a basis for $ker(A)$ (known as a [fundamentální systém (fundamental system)](https://felwiki.basta.one/en/Concepts/fundamentální-systém-fundamental-system_mc_fundamentální-systém-fundamental-system)), choose $d$ independent values for the free variables and then use backward substitution from the transformed equations to compute the remaining $s-d$ variables. Each choice yields a vector in the basis. Any solution to the homogeneous system is a linear combination of these basis vectors.

**Solving a Non-homogeneous System ($A \mathbf{x} = \mathbf{b}$):**
1.  Apply GEM to $(A | \mathbf{b})$ to get $(A' | \mathbf{b}')$.
2.  First, check solvability using Frobenius's Theorem: $rank(A) = rank(A | \mathbf{b})$. If they are not equal, no solution exists.
3.  To find a [partikulární řešení (particular solution)](https://felwiki.basta.one/en/Concepts/partikulární-řešení-particular-solution_mc_partikulární-řešení-partikulární-řešení.md), set the free variables (those without pivots in $A'$) to zero and use backward substitution to solve for the pivot variables.
4.  The general solution is then the sum of this particular solution and the general solution to the corresponding homogeneous system (i.e., $\mathbf{p} + ker(A)$).

An illustrative example was provided for solving $2x_1 + 3x_2 - 4x_3 = 2$ over $\mathbb{R}$. The augmented matrix is $(2 \ 3 \ -4 \ | \ 2)$. Here, $rank(A) = 1$ and $def(A) = 2$. The pivot is in the first position, meaning $x_2$ and $x_3$ are free variables.
*   The general solution form is $x = \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix} + a \begin{pmatrix} -3/2 \\ 1 \\ 0 \end{pmatrix} + b \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}$, where $\mathbf{p} = \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix}$ is a particular solution, and $a \begin{pmatrix} -3/2 \\ 1 \\ 0 \end{pmatrix} + b \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}$ represents the solutions to the homogeneous system. Geometrically, this solution describes a plane in $\mathbb{R}^3$.

The lecture concluded by demonstrating the application of GEM to a more complex system, emphasizing the notation for row operations and illustrating how the final solution (in this case, a line in $\mathbb{R}^4$) is obtained by identifying pivots, choosing free variables, and performing backward substitution.

### Conclusion and Key Takeaways

This lecture provided a foundational understanding of solving linear systems using Gaussian Elimination. Key takeaways include:
*   The matrix representation of linear systems ($A \mathbf{x} = \mathbf{b}$ and $(A | \mathbf{b})$).
*   The two perspectives on solutions: geometric intersection and linear combination of column vectors.
*   The definition and properties of matrices in upper block form, including the concept of pivots.
*   The three [řádkové elementární úpravy](https://felwiki.basta.one/en/Concepts/řádkové-elementární-úpravy-elementary-row-operations_mc_řádkové-elementární-úpravy-elementary-row-operations) and their role in transforming systems into equivalent forms.
*   The crucial [Frobeniova věta](https://felwiki.basta.one/en/Concepts/frobeniova-věta-frobenius-theorem_mc_frobeniova-věta-frobenius-theorem) for determining system solvability based on matrix [hodnost matice](https://felwiki.basta.one/en/Concepts/hodnost-matice-rank-of-a-matrix_mc_hodnost-matice-rank-of-a-matrix) and [defekt matice](https://felwiki.basta.one/en/Concepts/defekt-matice-defect-of-a-matrix_mc_defekt-matice-defect-of-a-matrix).
*   The systematic process for solving [homogenní soustava](https://felwiki.basta.one/en/Concepts/homogenní-soustava-homogeneous-system_mc_homogenní-soustava-homogeneous-system) and non-homogeneous systems, utilizing [fundamentální systém](https://felwiki.basta.one/en/Concepts/fundamentální-systém-fundamental-system_mc_fundamentální-systém-fundamental-system) and [partikulární řešení](https://felwiki.basta.one/en/Concepts/partikulární-řešení-particular-solution_mc_partikulární-řešení-particular-solution).

**Keywords:** Lineární algebra, Gaussova eliminační metoda, Matice, Soustavy lineárních rovnic, Frobeniova věta