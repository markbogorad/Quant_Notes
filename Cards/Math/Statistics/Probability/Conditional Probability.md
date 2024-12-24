up:: [[Probability MOC]]
tags:: #Math
# Conditional Probability
- Probabilities change when more information is known
$$ P(A|B) = \frac{P(A \cap B)}{P(B)} $$
- The probability of A given B
	- Is equal to the probability of the intersection of A and B divided by the probability of B
- The heart of the [[Bayes Theorem]]
## Logic
- If you know event B has occurred, the sample space is reduced to B itself. **Now, within this reduced sample space, you look for the probability of A happening**. That's why you divide by P(B) — you're adjusting your perspective to the new reality where B is a given.
	- Basically zooming in on the part where the probability has occurred already (B) and seeing how likely A is to happen after that
		- Different from the probability of A in the original (larger) context -> need to divide by P(B)
## Image
	 ![[conditional-probability-pa-b.png]]
