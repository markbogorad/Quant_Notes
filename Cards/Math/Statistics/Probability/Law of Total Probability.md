up:: [[Probability MOC]]
tags:: #Math
# Law of Total Probability
- Think of this as a way of finding the probability of something by finding everything that could possibly happen
- Derive marginal probability from conditional probabilities
	- **Essentially weighted average of all conditional probabilities**
$$ P(A) = \sum_{i=1}^{n} P(A|B_i)P(B_i) $$
where:
- P(A) is the marginal probability of event A.
- P(A|B) is the conditional probability of event A given event B.
- P(B) is the probability of the event B​.

## Assumptions
- Need to be mutually exclusive events (can't happen at once)
- Set of events needs to be exhaustive -> must encompass the entire sample space