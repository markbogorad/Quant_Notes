up:: [[Probability MOC]]
tags:: #Math
# Pareto Distribution
- For modeling things with the 80-20 principle
	- 80% of effects are a result of 20% of the causes
	- Aka Pareto principle
### Key Characteristics:
- Shape Parameter $( \alpha )$: The parameter \( \alpha \) (alpha) is known as the shape parameter. It controls the "tail heaviness" of the distribution. A smaller \( \alpha \) indicates a heavier tail, meaning that larger values of \( X \) are more probable.
- **Support**: The random variable $( X )$ takes values in the interval $([1, \infty))$.

### Probability Density Function (PDF):
The [[Probability Density Function (PDF)]] of a Pareto distribution is defined as:
$$
f(x) =
\begin{cases}
\frac{\alpha}{x^{\alpha+1}}, & \text{if } x \geq 1, \\
0, & \text{if } x < 1.
\end{cases}$$
- Decreases by power law --> different scale yo [[Normal Distribution]]
### Notation:
The Pareto distribution with shape parameter $( \alpha )$ is denoted as:
$$X \sim \text{Par}(\alpha)$$
### Cumulative Distribution Function (CDF):
The [[Cumulative Distribution Function (CDF)]] of the Pareto distribution, which gives the probability that the random variable $( X )$ is less than or equal to a certain value $( x )$, is given by:
$$F_X(x) = 1 - \left(\frac{1}{x}\right)^\alpha, \quad \text{for } x \geq 1$$
### Mean (Expected Value):
The mean of a Pareto distribution is only defined when \( \alpha > 1 \). It is given by:
$$E[X] = \frac{\alpha}{\alpha - 1}, \quad \text{for } \alpha > 1$$
### Variance:
The variance of a Pareto distribution is only defined when \( \alpha > 2 \). It is given by:
$$\text{Var}(X) = \frac{\alpha}{(\alpha - 1)^2(\alpha - 2)}, \quad \text{for } \alpha > 2$$
### Relationship to [[Exponential Distribution]]
- If a random variable $X$ follows a Pareto distribution with parameter $α$, then the natural logarithm of $X$, denoted $Y=log(X)$, follows an Exponential distribution with the same parameter $α$.
	- Log of Pareto = exponential
- $\text{If } X \sim \text{Par}(\alpha) \text{ and } Y = \log(X), \text{ then } Y \sim \text{Exp}(\alpha)$
	- $F_Y(y) = P(Y \leq y)$

