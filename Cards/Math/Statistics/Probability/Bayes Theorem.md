up:: [[Probability MOC]]
tags:: #Math
# Bayes Theorem
- For finding inverse [[Conditional Probability]]
- Given the probability of B, B given A, and A given B, we can update likelihood of A after observing B.
$$ P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)} $$
$$ P(A|B) = \frac{P(B \cap A)}{P(B)} $$
$$P(A | B) = \frac{P(B | A) \cdot P(A)}{P(B | A) \cdot P(A) + P(B | A^c) \cdot P(A^c)}$$
where:
- P(A|B): probability of A given that B has occurred.
- P(B|A): probability of observing B given that A is true.
- P(A): prior probability of A (before observing B)
- P(B) is the marginal probability of B, and it acts as a normalizing constant.
Also:
$$ $$ 
## Practical example:
- you want to calculate the probability that a person has a certain disease given they’ve tested positive for it
- Bayes’ Theorem allows you to incorporate the overall rate of the disease in the population and the accuracy of the test into your calculation.