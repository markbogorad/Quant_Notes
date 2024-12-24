up:: [[Probability MOC]]
tags:: #Math
# Random Variables
- Probability is the study of randomness
- Randomness - the opposite of deterministic
	- Deterministic --> throw a ball the exact same way 10 times, all times will land on the exact same spot
- A **random variable** is a numerical value assigned to the outcomes of a random event. It represents a way to quantify the results of a random process, turning outcomes into numbers that can be analyzed mathematically.
	- Quantifying an outcome

## Differences in Types of Distributions

| **Distribution** | **When to Use**                                                                                                                                               | **PMF LaTeX Formula**                                                      | **Expectation LaTeX Formula**           | **Variance LaTeX Formula**                   |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------- | --------------------------------------- | -------------------------------------------- |
| **Uniform**      | When you have a finite set of equally likely outcomes over a range. <br>Example: Rolling a fair die.                                                          | $( P(k) = \frac{1}{b-a+1} )$<br>                                           | $( \mathbb{E}[X] = \frac{b+a}{2} )$<br> | $( \text{Var}(X) = \frac{(b-a+1)^2 - 1}{2})$ |
| **Bernoulli**    | When there are only two possible outcomes (success/failure) for a single trial. <br>Example: Flipping a coin (Heads or Tails).                                | $( P(k) = p \text{ if } k = 1, \text{ or } P(k) = 1-p \text{ if } k = 0 )$ | $( \mathbb{E}[X] = p )$                 | $( \text{Var}(X) = p(1-p) )$                 |
| **Binomial**     | For a fixed number of independent trials, each with the same probability of success. <br>Example: Number of heads in 10 coin flips.                           | $( P(k) = \binom{n}{k} p^k (1-p)^{n-k} )$                                  | $( \mathbb{E}[X] = np )$                | $( \text{Var}(X) = np(1-p) )$                |
| **Geometric**    | When interested in the number of trials needed to get the first success. <br>Example: Number of attempts before getting the first heads in coin flips.        | $( P(k) = p(1-p)^{k-1} )$                                                  | $( \mathbb{E}[X] = \frac{1}{p} )$       | $\text{Var}(X) = \frac{1-p}{p^2} )$          |
| **Poisson**      | When you are modeling the number of events in a fixed interval of time or space with a known average rate. <br>Example: Number of emails received in an hour. | $( P(k) = \frac{e^{-\mu} \mu^k}{k!} )$                                     | $( \mathbb{E}[X] = \mu t )$             | $( \text{Var}(X) = \mu t )$                  |


