# Richardsonova extrapolace

## Summary
A method used to improve the accuracy of a sequence of approximate results obtained from a numerical method, based on the formula F(h) = F(0) + ahp + O(hq), where q > p.

## Detailed Explanation
Richardson extrapolation is a powerful numerical analysis technique employed to enhance the accuracy of approximate results. It is applied when a numerical method produces an approximation $F(h)$ that depends on a step size $h$. The method's effectiveness hinges on the assumption that the error in the approximation can be expressed as a series expansion involving powers of $h$. Specifically, as stated in its definition, it is based on the formula $F(h) = F(0) + ah^p + O(h^q)$, where $F(0)$ is the true value, $ah^p$ represents the dominant error term with $p$ being the order of the method, and $O(h^q)$ represents higher-order error terms where $q > p$. By combining approximations obtained with different step sizes (e.g., $h$ and $h/2$), Richardson extrapolation algebraically eliminates the lowest-order error term, thereby producing a new, more accurate estimate of $F(0)$. This process effectively accelerates the convergence of the numerical method.

## Importance/Relevance
This concept has an importance score of 0.7. Richardson extrapolation is highly important because it allows for significant improvements in the accuracy of various numerical methods (like differentiation and integration) without requiring a substantial increase in computational effort, making it a valuable tool in computational mathematics.

## Connections
### Appears In Lectures
- Mathematical Analysis: Integrals, Series, and Numerical Methods

## Category
Numerical Analysis Technique