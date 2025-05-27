# Výpočet determinantu pomocí GEM

## Summary
Výpočet determinantu pomocí Gaussovy eliminační metody (GEM) je metoda pro výpočet determinantu pomocí řádkových operací. Při tom je důležité si pamatovat, že záměna řádků mění znaménko determinantu, vynásobení řádku skalárem změní determinant a-krát, a přičtení lineární kombinace jednoho řádku k jinému nemění hodnotu determinantu. Determinant horní trojúhelníkové matice je součin prvků na diagonále.

## Detailed Explanation
### Definition
According to the lecture "Determinant: část 1" (ID: 07A-2024-Determinant-Part-1):
> Metoda pro výpočet determinantu pomocí řádkových operací. Záměna řádků mění znaménko, vynásobení řádku skalárem změní determinant a-krát, přičtení lineární kombinace nemění hodnotu. Determinant horní trojúhelníkové matice je součin prvků na diagonále.

This method leverages the properties of elementary row operations on determinants. By transforming a matrix into an upper triangular form (or row echelon form) using Gaussian elimination, the determinant can be easily calculated as the product of its diagonal elements. However, careful tracking of the row operations is essential:
*   **Row Swaps:** Each swap of two rows negates the determinant.
*   **Row Scaling:** Multiplying a row by a scalar `c` multiplies the determinant by `c`.
*   **Row Addition:** Adding a multiple of one row to another row does *not* change the determinant.

## Importance/Relevance
This concept is an important and efficient method for calculating determinants, especially for larger matrices where the Leibniz formula or Sarrus' Rule (for 3x3) become unwieldy.

## Connections
### Appears In
*   [Determinant: část 1](07A-2024-Determinant-Part-1)

### Category
Calculation Method