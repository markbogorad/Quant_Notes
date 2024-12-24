up:: [[Probability MOC]]
tags:: #Math
# CDF
- Think of this as tracking **accumulated probabilities**
- The **CDF** $( F_Y(a) )$ of a random variable $( Y )$ is a function that gives the probability that $( Y )$ is less than or equal to a certain value $( a )$. 
- In other words:
	- $F_Y(a) = P(Y \leq a)$
		- Probability (CDF) of Y evaluated at A
		- $( F_Y(a) )$: This represents the value of the CDF of $( Y )$ at the point $( a )$.
### Interpretation
- For any given value $( a )$, $( F_Y(a) )$ tells you how likely it is that the random variable $( Y )$ will be less than or equal to $( a )$.
- The function $( F_Y(a) )$ is non-decreasing and ranges from 0 to 1 as $( a )$ moves from negative infinity to positive infinity.
### Example
- If $( Y )$ is the result of rolling a fair 6-sided die, and $( a = 3 )$, then:
	- $F_Y(3) = P(Y \leq 3) = P(Y = 1) + P(Y = 2) + P(Y = 3)$
- Given that each side of the die has an equal probability of $( \frac{1}{6} )$, you would have:
	- $F_Y(3) = \frac{1}{6} + \frac{1}{6} + \frac{1}{6} = \frac{3}{6} = 0.5$
- This means there is a 50% probability that the outcome of rolling the die will be 3 or less.

### Graphically
- ![[Pasted image 20240825105229.png]]
- [[Probability Density Function (PDF)]]