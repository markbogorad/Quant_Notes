up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning 
# Ridge Regression (L2)
- Ridge regression is when you add the L2 penalty term to a linear [[Regression]]
- Uses L2 penalty
$$\text{Penalty} = \alpha * \Sigma{w_n^2}$$
- Penalty is the sum of all weights squared 
	- **Weights can not go to 0**
- In ridge regression we seek the vector of weights that minimize either of the two equivalent expressions of
- Similar to [[Lasso Regression]] but never leads to a 0 value for a coefficient (is asymptotical and will reach close to 0)
$$\begin{aligned} \hat{w}^\mathrm{ridge} =& \text{argmin}_w \sum_{n=1}^N \left( y^{(n)} - w^\top x^{(n)} \right)^2 + \lambda \Vert w \Vert^2 \\ =& \text{argmin}_w \Vert y - X w \Vert^2 + \lambda \Vert w \Vert^2. \end{aligned}$$
- Here, $\Vert w \Vert^2$ is the ridge regularization penalty, and $\lambda$ is the regularization constant.
## Pros & Cons
**Pros:**
- Ridge regression is quite fast. Without any extra computation, it is possible to get a solution for all the selected values of $\lambda$ by solving the equation once.
- It is also stable as the weights change very gradually with respect to change in $\lambda$.
- In practice, ridge regression generalizes better compared to other methods. Specifically, when we use any regularization method, we get a space of different weights $w$. In general, the best $w$ obtained from using ridge regression with linear methods performs better on the test data than the $w$ from any other method.

Because of these advantages, Ridge regression is used more often than other methods.