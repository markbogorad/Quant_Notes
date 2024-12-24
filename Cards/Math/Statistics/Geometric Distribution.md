up:: [[Probability MOC]]
tags:: #Math 
# Geometric Distribution
- **Models how many trials it take before you see a first success**
- This is the result of multiple [[Bernoulli Random Variable & Processes]] experiments
- "Probability distribution that models the number of trials needed to get the first success in a sequence of independent and identically distributed (i.i.d.) Bernoulli trials."
- [[Probability Mass Function (PMF)]]
    - $P(X=k)=(1−p)^{k−1}⋅p$
		- $p$ is the probability of success on each trial.
	    - $k$ is the trial number on which the first success occurs.
- [[Expectation]]
    - $E(X)=\frac{1}{p}$
- [[Variance]]
	- $Var(X)=\frac{1−p}{p^2}$
## Murphy's Law
- Probability of a success / failure
-  Murphy's Law --> of any chance of success, then you will eventually succeed (geometric with infinite trials) and vice versa for failure