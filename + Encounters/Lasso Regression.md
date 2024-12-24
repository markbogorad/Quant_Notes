up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# Lasso Regression
- Penalizes additional features
- Lasso regression is very similar to [[Ridge Regression]]. The only difference between them is that in lasso regression, we use the absolute value of all components of w instead of taking the square root of the sum of squared values. Lasso regression is defined as follows:
$$\hat{w}^{\mathrm{lasso}} = argmin_{w} \sum_{n=1}^{N} (y^{(n)} - w^\top x^{(n)})^{2} + \lambda \sum_{i=1}^{D} \vert w_{i} \vert$$
- The derivative of |w| isn't defined when w=0 (because of the corner point in the graph of |w|). This means during optimization, a weight can directly hit zero and stay there, making the solution sparse. We have no good closed-form solution for \hat{w}^\text{lasso} as it is not easily differentiable.
## Pros & Cons
**Pros:**
- Lasso Regression is fast. Even though there isn't a closed-form solution, there are algorithms designed for lasso that are similarly fast in practice (e.g. [LARS](https://en.wikipedia.org/wiki/Least-angle_regression)).
- It is also more stable than the previously discussed methods, meaning the weights change gradually as $\lambda$ changes.
- We obtain sparse solutions with the lasso, especially when the regularization constant is large. This is mainly because, as can be seen from the visualization above. Since the regularization is "sharp" near zero, large enough regularization can make certain terms zero.

**Cons:**
- The lasso often generalizes a bit worse than the ridge regression in practice.