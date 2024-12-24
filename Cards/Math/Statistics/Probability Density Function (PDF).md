up:: [[Probability MOC]]
tags:: #Math
# PDF
- A **probability density function (PDF)** is a function that describes the likelihood of a [[Continuous Random Variables]] taking on a particular value
	- Used for **continuous random variables**, not discrete. The discrete equivalent is [[Probability Mass Function (PMF)]]
- Probabilities are counted over intervals, not specific points
## Mathematically
- For a continuous random variable X, the probability density function, denoted by $f(x)$, **describes the relative likelihood that $X$ will take on a specific value.**
- Mathematically, the PDF $f(x)$ is defined such that the probability that $X$ lies within a particular interval $[a,b]$ is given by the integral of $f(x)$ over that interval: 
	- $P(a \leq X \leq b) = \int_a^b f(x) \, dx$

## Condition for Normalization
- For the PDF to follow a normal, this condition must be met:
	- $\int_{-\infty}^{\infty} f(x) \, dx = 1$
		- Just means the entire range of possible values is 1

## Example
- Consider a [[Continuous Random Variables]] X that is uniformly distributed between 0 and 1. The PDF of X is:
$$f(x) = \begin{cases} 
1 & \text{if } 0 \leq x \leq 1 \\
0 & \text{otherwise}
\end{cases}$$
- This means that X is equally likely to take any value between 0 and 1.
