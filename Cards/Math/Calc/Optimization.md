up:: [[Calculus MOC]]
tags:: #Math
# Optimization
$$\mathcal{L}(x, y, \lambda) = \textcolor{green}{f(x, y)} + \lambda \left[ \textcolor{yellow}{g(x, y)} \right]$$
- Maximizing or minimizing a function, often with constraints (constrained optimization)
- **Linear programming:**
	- When the objective function and constraints are linear
- **Non-linear programming (NLP):**
	- When the objective function and/or the constraints are non-linear
	- Often used in [[Machine Learning Miscellaneous MOC]]
	- Solved using [[Lagrange Multiplier]]

## Quadratic Optimization
- Mixes in [[Linear Algebra MOC]]
$$\min \frac{1}{2} w' \Sigma w \hspace{2cm} st: w'1 = 1 \quad \text{and} \quad w'r = R$$
- Lagrangian is:
	- $L = \frac{1}{2} w' \Sigma w - \lambda (w'1 - 1) - \gamma (w'r - R)$
- This represents a quadratic optimization problem typical in portfolio optimization (this is a [[Quadratic Forms]])
	- $w$ is the weight vector of the assets in the portfolio.
	- $Σ$ is the covariance matrix of the asset returns.
- The objective is to minimize the portfolio variance (risk).
- The constraints are that the sum of weights equals 1 (fully invested portfolio) and the portfolio returns equal $R$.
- $L$ is the Lagrangian function used to solve this constrained optimization problem, with $λ$ and $γ$ as the Lagrange multipliers.

