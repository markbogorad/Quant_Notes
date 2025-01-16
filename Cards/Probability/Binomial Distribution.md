up:: [[Probability MOC]]
tags:: #Math
# Binomial Distribution
- Sum of [[Bernoulli Random Variable & Processes]] trials
	- the **number of successes** in a fixed number of binary trials
- Notation
	- $y∼Bin(n,p)$
		- y follows a binomial distribution with parameters n and p
	- If n = 6 and p = 0.7, there are 6 trials with a 0.7 probability of success in each trial
- [[Probability Mass Function (PMF)]]
- The probability of getting exactly $k$ successes in n trials is given by the binomial formula:
	- Intuitively: Number of Orderings (from [[Binomial Coefficient (Permutations)]]) $\times$ probability of said ordering (everything to the right side)

$$P(X = k) = \binom{n}{k} p^k (1 - p)^{n - k}$$
where:
$$\binom{n}{k} = \frac{n!}{k!(n-k)!}$$
- **Number of Trials (n):** The total number of trials or experiments conducted.
- **Probability of Success (p):** The probability of success on each individual trial.
- **Number of Successes (k):** The number of successes you are interested in finding the probability for.
- [[Expectation]]
	- $\mathbb{E}[X] = np$
- [[Variance]]
	- $\text{Var}(X) = np(1-p)$
