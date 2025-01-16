up:: [[Probability MOC]]
tags:: #Math 
# Uniform Distribution
- A **uniform distribution** is a type of probability distribution where **all outcomes are equally likely** within a certain interval.
## Discrete Case
- Ex: rolling a die (all outcomes have the same probability)
- Discrete Uniform Distribution:}
	- $X \sim \text{Uniform}(a, b), \quad \text{where } a, a+1, \dots, b \text{ are integers.}$
- [[Probability Mass Function (PMF)]]
	- $P(X = k) = \frac{1}{b-a+1}, \quad \text{for } k = a, a+1, \dots, b$
- [[Expectation]]
	- $\mathbb{E}[X] = \frac{b+a}{2}$
- [[Variance]]
	- $\text{Var}(X) = \frac{(b-a+1)^2 - 1}{12}$
## Continuous Case
- Definition: In a continuous uniform distribution, every value within a specified interval is equally likely to occur. The distribution is described by a constant probability density function (PDF) over this interval.
- [[Probability Density Function (PDF)]]
	- $f_X(x) = \begin{cases} \frac{1}{b - a}, & \text{if } a \leq x \leq b, \\ 0, & \text{otherwise}. \end{cases}$
- [[Expectation]]
	- $\mathbb{E}[X] = \frac{b+a}{2}$
- [[Variance]]
	- $\text{Var}(X) = \frac{(b-a)^2}{12}$
	