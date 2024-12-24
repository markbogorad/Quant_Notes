up:: [[Probability MOC]]
tags:: #Math
# Notation
## Quick set theory notation
### Universal Set:
$$ S \quad \text{or} \quad \Omega $$
- Description: The set of all possible outcomes in a given context
### Subset:
$$ A \subseteq B $$
- Description: Set A is a subset of set B if **every element of A is also an element of B**.
### Proper Subset:
$$ A \subset B $$
- Set A is a proper subset of B if **A is a subset of B** and A≠B.
### Set Difference
$$ A \setminus B $$
- Description: The set of all elements that are **in A but not in B**.
### Disjoint sets
$$ A \cap B = \emptyset $$
- Description: Sets AA and BB are disjoint if they have **no elements in common.**
### Power set
$$ \mathcal{P}(A) $$
- Description: The set of all subsets of A, including the empty set and A itself.
### Cardinality
$$ |A| $$
- Description: The **number of elements** in set A.


## Probability
$$ P(A) $$
- Represents the probability of event A happening
	- Ex: P(rain today)
## Conditional Probability
$$ P(A \mid B)
 $$
- Represents the probability of even A happening, given event B also occurs
	- P(rain | cloudy)
## Joint Probability
$$ P(A \cap B) =  P(A) + P(B) + P(A^c \cap B^c) - 1  $$
- Probability of both events occurring together
	- The **intersection** of A and B
## Complementary Probability
$$ P(A^c) \quad \text{or} \quad P(\neg A) $$
- The probability of A not happening
- Can apply this to probability theories by making entire formulae complements
	- Ex (**union of complementary events**): $$ P(A^c \cup B^c) = P(A^c) + P(B^c) - P(A^c \cap B^c) $$
## Union of events
$$ P(A \cup B) = P(A) + P(B) - P(A \cap B) $$
- This is the probability of event A happening, event B happening, or both
	- **A + B - their intersection**
## Independent Events
- 2 events are independent if:
$$ P(A \cap B) = P(A)P(B) $$
- Occurrence of A does not affect the occurrence of B
- Alternative notation
$$ E_1 \perp\!\!\!\perp E_2 $$
	- Outcome of E1 wont influence E2
-


