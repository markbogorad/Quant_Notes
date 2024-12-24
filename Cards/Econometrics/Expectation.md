up:: [[Probability MOC]]
tags:: #Math
# Expectation
- A concept from [[Probability MOC]]
- The expectation of a random variable $X$ is denoted by $E[X]$
- It is a rough average of the random variable over X experiments
- **It is the sum of all outcomes for a random variable multiplied by their probability**
## Mathematical Definition
- Discrete random variables:
	- $E[X] = \sum_{i} x_i p_i$
	- Multiplying each $x$ variable by its probability $p$
	- This is commonly used in dice roll brainteasers
	
- Continuous random variables
	- $E[X] = \int_{-\infty}^{\infty} x f(x) \, dx$
	- Integrate the product of the value and its density over the entire range of the variable.
		- [[Probability Density Function (PDF)]] is the right bit
## Properties of Expectation
- Linearity  
	- $E[aX + bY] = aE[X] + bE[Y]$
	- expectations are **additive**
	- A and B do not depend on the outcome of the experiment
- Constant
	- $E[c] = c$
- Sum of expectations
	- $E\left[\sum_{i=1}^{n} X_i\right] = \sum_{i=1}^{n} E[X_i]$
	- Expectation of the sum is equal to the sum of expectations
- Non negativity
	- $E[X] \geq 0$
	- If x is non negative, expectation must also be non-negative
## Conditional Expectation
- $E[C_2 | C_1] = \alpha + \beta C_1$
- Variance included:
	- $E[C_2 | C_1] = \mu_2 + \beta (C_1 - \mu_1)$
	- $\text{Var}(C_2 | C_1) = \sigma_{22} - \frac{\sigma_{12}^2}{\sigma_{11}}$
	
## Relationship to Distribution
- Knowing distribution tells you expectation
- $E[p(x)] = sigma p(i) p(x=i)$

## Expectation of a Function
- Apply the function to the X component only and recalculate
- Ex: what is the expectation of $X^2$ for a fair dice throw
- $E[X^2] = \sum_{i} (x_i)^2 p_i$