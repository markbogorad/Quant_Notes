up:: [[Probability MOC]]
tags:: #Math
# Outcomes:
- Aka permutations and combinations
## Independent trials
- Here, its just the multiplication of the number of outcomes 
$$ n^k $$
where
- N is the number of outcomes per trial
- K is the number of trials
Example:
- Flipping a coin 3 times = 2^3 = 8
- MCQ test with 3 questions and 4 choices: 4^3 = 64
## Dependent trials
- Multiply the number of outcomes for each stage
$$ n_1 \times n_2 \times \ldots \times n_k $$
Example:
- Drawing 2 cards out of a deck: 52 * 51
	- First draw has 52 possible outcomes, 2nd one now has 51

## Permutations method from GMAT
**If order doesn't matter (combinations):**
$$ \frac{N!}{(N-K)!K!} $$
where:
- N is the amount of options
- K is the amount of items
Example: 
- Flying to 10 potential destinations, need to pick 4
	- N = 10, K = 4

**If order matters (permutations):**
$$ P(N, k) = \frac{N!}{(N-k)!} $$
- This calculates the **number of distinct ways k items can be ordered** when chosen from a set of N items.
