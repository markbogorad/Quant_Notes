up:: [[Probability MOC]]
tags:: #Math 
# Variance
- **Variance** is a measure of the spread or dispersion of a random variable's possible values around its expected value (mean). It quantifies how much the values of a random variable differ from the expected value on average.
	- See [[Expectation]]
$$\text{Var}(X) = \mathbb{E}[(X - \mathbb{E}[X])^2]$$
- Expected value of X minus the expected value of X
	- X is deterministic --> x does not depend on omega (state of world), it is purely a constant
or
$$\text{Var}(X) = \mathbb{E}[X^2] - (\mathbb{E}[X])^2$$
- Expected value of (X squared) minus expected value of (X) squared

- You can multiply random variables by constants when computing variance
	- Linearity of [[Expectation]]
- Because the formula for expectation is sum of all outcomes $\times$ the probabilities of those outcomes, variance has a unique characteristic in it's definition with expectation
	- **Square of expectation of X is not the same as expectation of X squared!**

- The **$(X−E[X])^2$ term is
	- The squared deviation of XX from its mean. This measures how far each value of XX is from the mean, and squaring it ensures that deviations in both directions (above and below the mean) contribute positively.
- So $E[(X−E[X])^2]$
	- The expected value of the squared deviations gives the average of these squared deviations, which is the variance.
	
- Variance of sum is sum of variances
	- The principle that "the variance of a sum is the sum of variances" underlines the idea that if you have a set of independent random variables, the total variability (variance) of their combined effect is just the sum of their individual variabilities



