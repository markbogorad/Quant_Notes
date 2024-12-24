up:: [[Probability MOC]]
tags:: #Math 
# Martingales
$$E(X_{n+1} \mid X_1, X_2, \dots, X_n) = X_n$$
- The expected future value given you have history of the past is equal to the current value
## Proving a Martingale
- Need to show that the process has no drift (systematic increase or decrease through time)
- ALSO need to show that $E[X_i] = 0$
	- Expected value of the next increment is 0 given the current information
- Show that:
	- $E(X_{n+1} \mid X_1, X_2, \dots, X_n) = X_n$
	- Most commonly done by proving independence then crossing out P(B) in bayes theorem formula
- Ways to prove
	- **[[Independence]]**
		- This brings in the fact that the equation will equal $X_n$
			- Set up problem in the framework of conditional probability
	- **Constants**
		- Any constants that get in the way we can factor out (linearity of [[Expectation]] property)
		- Must prove that the constant is determined by the information conditioned on (right side of conditional probability)
### Key Steps
- Basically try to frame the given stuff under the martingale property formula, then prove it is equal to the current state by independence.
- Set up martingale condition
- Take conditional expectation
- Use independence
- Impose martingale condition
- Prove that $E[X_i] = 0$