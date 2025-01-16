up:: [[Probability MOC]]
tags:: #Math
# Correlation
- Describes the strength and direction of a linear relationship between two random variables. Unlike covariance, which can take any value depending on the scale of the variables, correlation is a normalized measure that is always between -1 and 1.
	- [[Correlation vs Covariance]] -> this is standardized covariance to a range of -1 to +1
$$\rho_{XY} = \frac{\text{Cov}(X, Y)}{\sigma_X \sigma_Y}$$
$$\rho_{X,Y} = \frac{\text{Cov}(X, Y)}{\sqrt{\text{Var}(X)} \cdot \sqrt{\text{Var}(Y)}}$$
- $Cov(X,Y)$ is the covariance between X and Y.
- $σ_X$​ is the standard deviation of X.
- $σ_Y$​ is the standard deviation of Y.
## Properties of Correlation
- **Symmetry**: Correlation is symmetric, meaning $ρ_{XY}=ρ_{YX}$
- **Unitless**: Correlation is a dimensionless quantity, meaning it does not depend on the units in which X and Y are measured.
- **Invariance to Scaling and Shifting**: Correlation remains unchanged if you scale or shift the variables. For example, if you transform X to aX+b and Y to cY+d the correlation between the transformed variables remains the same as between the original variables.

- expexcted value of y cobditional on x can be written as A + B --> linear function of x

## In [[Machine Learning Miscellaneous MOC]]
- If both features 1 and 2 are above this said average, then they have a positive relationship
- Look at notion slides week 5