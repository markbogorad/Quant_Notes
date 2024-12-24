up:: [[Probability MOC]]
tags:: #Math
# Poisson Distribution
- A probability distribution that models the **number of events occurring** within a **fixed interval of time** or space, under the assumption that these events happen independently and at a constant average rate.
$$X∼Poisson(λ)$$
- **Rate Parameter (λ)**: This is the average number of occurrences in the given interval. It’s both the mean and the variance of the distribution.
- **Number of Occurrences (k)**: The number of times an event occurs in the interval.
- [[Probability Mass Function (PMF)]]
$$P(k) = \frac{e^{-\mu} \mu^k}{k!}$$
	- $λ$ is the average rate (mean number of events) over the interval.
	- $k!$ is the factorial of $k$, representing the number of ways $k$ events can occur.
	- $e$ is the base of the natural logarithm, approximately equal to 2.71828.
- Sub intervals of the poisson are [[Bernoulli Random Variable & Processes]]
- [[Expectation]]
	- $\mathbb{E}[X] = \mu t$
- [[Variance]]
	- $\text{Var}(X) = \mu t$

