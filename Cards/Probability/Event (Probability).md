up:: [[Probability MOC]]
tags:: #Math
# Event
- In probability theory, an **event** is a subset of the sample space, which is the set of all possible outcomes of a random experiment. Formally, given a sample space ($\Omega$), an event ($A$) is a subset of ( $\Omega$), i.e., $(A \subseteq \Omega )$. 
	- [[Set Theory]]
- An event can consist of one outcome, multiple outcomes, or no outcomes at all:
	- If $( A = {\omega})$, where $( \omega )$ is an element of $( \Omega )$, the event $( A )$ is called a **simple event** or **elementary event**.
	- If \( A = \Omega \), the event $( A )$ is the **sure event**, meaning it will always occur.
	- If $( A = \emptyset$), the event $( A )$ is the **impossible event**, meaning it will never occur.

The probability of an event $( A )$, denoted by $( P(A) )$, is a measure that satisfies the following [[Probability Axioms]]:

1. **Non-negativity**: $( P(A) \geq 0 )$ for any event $( A )$.
2. **Normalization** (unitarity): $( P(\Omega) = 1 )$.
3. **Additivity**: For any two mutually exclusive events $( A )$ and $( B )$ (i.e., $( A \cap B = \emptyset )$), the probability of their union is the sum of their probabilities: $( P(A \cup B) = P(A) + P(B) )$.

## How many events in a sample space
- General formula:
	- Outcomes per trial ^ amount of trials
	- Ex: coins --> $2^n$ where n is amount of times you throw coin

