up:: [[Probability MOC]]
tags:: #Math
# Conditional Expectation
## Discrete
$$E[\varphi(X) \mid Y = y] = \sum_{x \in D} \varphi(x) \cdot P(X = x \mid Y = y)$$
- $E[φ(X)∣Y=y]$: This is the conditional expectation of $φ(X)$ given that $Y=y$.
- $∑x∈D​$: This is a summation over all possible values xx that XX can take, which are in the domain DD.
- $φ(x)$: This is the function φφ applied to the value xx.
- $P(X=x∣Y=y)$: This is the conditional probability that $X$ equals $x$ given that $Y=y$.

## Continuous
$$E[X \mid Y = y] = \int_{-\infty}^{\infty} x \cdot f_{X \mid Y}(x \mid y) \, d$$
- $E[X∣Y=y]$ represents the expected value of $X$ when $Y$ is fixed at $y$.
- $fX∣Y(x∣y)$ is the conditional probability density function (PDF) of $X$ given $Y=y$.
- The integral computes the weighted average of all possible values of $X$, weighted by their conditional probability when $Y=y$.
## Continuous Conditional Variance
$$\text{Var}[X \mid Y = y] = \int_{-\infty}^{\infty} \left(x - E[X \mid Y = y]\right)^2 \cdot f_{X \mid Y}(x \mid y) \, dx$$
- $Var[X∣Y=y]$ is the variance of $X$ given that $Y=y$.
- $E[X∣Y=y]$ is the conditional mean (expected value) of $X$ given $Y=y$.
- The expression $(x−E[X∣Y=y])^2$ measures the squared deviation of $X$ from its conditional mean.
- The integral calculates the average of these squared deviations, weighted by the conditional PDF $fX∣Y​(x∣y)$.
