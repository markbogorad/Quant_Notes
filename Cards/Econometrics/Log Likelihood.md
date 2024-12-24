up:: [[Probability MOC]], [[Econometrics MOC]]
tags:: #Math
# Log Likelihood
- The probability of the observed data given a set of parameter values for a statistical model
**Likelihood Function**
$$ % Likelihood Function
L(\theta) = \prod_{i=1}^n f(y_i; \theta)
% Log-Likelihood Function
\ell(\theta) = \log L(\theta) = \sum_{i=1}^n \log f(y_i; \theta) $$
- **L(θ)** : This is the likelihood function, which gives the probability of the observed data given the parameters θ of the model.
- **θ**: These are the parameters of the statistical model that we are trying to estimate.
	- Ex: in [[Multiple Linear Regression]], theta is:
		- θ=(β0​,β1​,σ2)
			- β0​: The intercept parameter.
			- β1​: The slope parameter.
			- σ^2: The variance of the error term ϵ.
			- For [[ARIMA]] stuff, this could be actual AR and MA components
- **{y1​,y2​,…,yn​}**: This is the set of observed data points. Each yi​ is an individual observation.
- **f(yi​;θ)**: This is the probability density function (pdf) or probability mass function (pmf) for the i-th observation yi​ given the parameters θ. *It describes the likelihood of observing yi​ given θ.*
- **∏​**: This denotes the product of the individual probabilities f(yi​;θ) for all observations from i=1to i=n.

**Log Likelihood Function**
*Intuition:*
Taking the logarithm of the likelihood function converts the product of probabilities into a sum, which is mathematically more tractable. The log-likelihood function retains the property that maximizing the log-likelihood is equivalent to maximizing the original likelihood.
$$ \ell(\theta) = \log L(\theta) = \sum_{i=1}^n \log f(y_i; \theta) $$
- **ℓ(θ)**: This is the log-likelihood function, which is the *natural logarithm of the likelihood function.*
- **logL(θ)**: Taking the logarithm of the likelihood function. The log transformation simplifies the product of probabilities into a sum, making it easier to work with, especially for differentiation and maximization.
- **∑i=1n​**: This denotes the sum of the logarithms of the individual probabilities f(yi​;θ) for all observations from i=1 to i=n.

The log-likelihood function simplifies the complex product into a more manageable sum, and this form is what is typically used in practice for parameter estimation via [[Maximum Likelihood Estimator]] estimation.