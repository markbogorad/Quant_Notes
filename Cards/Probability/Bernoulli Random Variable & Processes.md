up:: [[Probability MOC]]
tags:: #Math 
# Bernoulli Process
- Number of successes in n trials
- A Bernoulli process is a sequence of independent and identically distributed (i.i.d.) random variables, each of which has two possible outcomes: success (usually coded as 1) and failure (usually coded as 0) --> aka **bivariate outcomes**
	- Used in [[Lattice Methods]]
	- Used for modeling trials with only 2 possible outcomes --> success vs failure
- $P_X(x) = \begin{cases} p, & \text{if } x = 1, \\ 1-p, & \text{if } x = 0, \\ 0, & \text{otherwise}.\end{cases}$
	- basically P or P-1 in the sample space
	- Success (1) failure (0)
- [[Expectation]]
	- $\mathbb{E}[X] = p$
- [[Variance]]
	- $\text{Var}(X) = p(1-p)$
## Sum of Bernoulli Variables
- This models the successes after N trials
- [[Binomial Distribution]]
