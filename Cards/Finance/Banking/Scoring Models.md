up:: [[Banking MOC]]
tags:: #Finance 
# Quantitative Scoring Models for Credit Risk
- **How they work:** use certain metrics to divide borrowers into distinct categories
	- **Firms:** profitability, leverage, size
	- **Individuals:** income, rent/own, type of job, marital status
## Linear Discriminant Models
- Looks similar to a [[Multiple Linear Regression]], [[Econometrics MOC]]
- Discriminant: maximizes likelihood of separating population into defaulters and non defaulters
- Intended to match characteristics with defaults
- Use [[Eigenvalues]] for maximization ([[General Math MOC]])
### Altman Z-score Model
$$Z = 1.2X_1 + 1.4X_2 + 3.3X_3 + 0.6X_4 + 1.0X_5 $$
- X1​ = Working capital / total assets
- X2 = Retained earnings / total assets
- X3​ = EBIT / total assets
- X4​ = Market value equity / book value LT debt
- X5​ = Sales / total assets
- Z -> measures likelihood of default (between 0 and 1)

**Cut off values:**
- Z > 2.99 - "Safe" Zones
- 1.81 < Z < 2.99 - "Grey" Zones
- Z < 1.81 - "Distress" Zones
## Linear Probability Models
$$  PD_i = \sum_{j=1}^{n} \beta_j X_{i,j} + \text{error} $$
- Not statistically sound -> default probabilities are not really probabilities
## Logit Models
$$ \log \left( \frac{PD}{1 - PD} \right) = \beta_0 + \beta_1 X_1 + \beta_2 X_2 + \cdots + \beta_n X_n $$
- Where
	- PD is the probability of default.
	- β0,β1​,…,βn​ are the coefficients.
	- X1,X2,…,Xn are the predictor variables.
- A transformation of the Linear Probability Model
- Uses logistic regression ([[Machine Learning Miscellaneous MOC]]) and [[Maximum Likelihood Estimator]]
	- Overcomes linear probability models shortcoming by restricting probabilities to only 2 states (default or no default)