up:: [[Econometrics MOC]]
tags:: #Math
# OLS Estimator
- **Goal:** find the best-fitting line through the data points by *minimizing the sum of the squared differences* between the observed values and the values predicted by the linear model
$$ \text{Minimize} \sum_{i=1}^n (y_i - \hat{y}_i)^2 $$
- where Yi hat is the predicted value of Yi
## How it works
- OLS are derived by taking [[Partial Derivatives]] of the sum of squared residuals with respect to B0 and B1, setting them to 0, and finding the resulting parameters

## Gauss Markov Assumptions
1. **Linearity**: The relationship between the dependent and independent variables is linear.
$$ \begin{equation} y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \cdots + \beta_n x_n + \epsilon \end{equation} $$

2. **Independence**: The observations are independently and identically distributed (i.i.d).
$$ \begin{equation} \text{Cov}(\epsilon_i, \epsilon_j) = 0 \quad \text{for} \quad i \neq j \end{equation} $$

3. **Homoscedasticity**: The variance of the error terms is constant across all levels of the independent variable.
$$ \begin{equation} \text{Var}(\epsilon_i) = \sigma^2 \quad \text{for all} \quad i \end{equation} $$
4. **No perfect multicollinearity**: The independent variables are not perfectly correlated.
$$ \begin{equation} \text{rank}(X) = k \end{equation} $$
5. **Normality of errors**: The error terms are normally distributed (optional, but useful for inference).
$$ \begin{equation} \epsilon_i \sim \mathcal{N}(0, \sigma^2) \end{equation} $$
