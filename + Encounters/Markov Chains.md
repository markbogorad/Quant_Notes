up:: [[Probability MOC]]
tags:: #Math
# Markov Chains
$$P(X_n|X_0, X_1, ...,X_n) = P(X_n|X_{n-1})$$
- a mathematical model that describes a sequence of possible events, where the probability of each event depends only on the state attained in the previous event. This property is known as the **Markov property**, which means the process has "no memory" — the future state only depends on the present state and not on the sequence of events that preceded it.
	- You can basically ignore everything about the process except the last observation (**statement on the past**)
- General form (transition matrix)
- ![[Markov-jump-processes-with-three-discrete-states-The-transition-rate-matrix-Q-ESS 1.png]]
	- The probability of going from state 1 to state 2 is designed by $q_{12}$
## Prove that something is a Markov Chain
- Need to prove the Markov property
	- $P(X_n|X_0, X_1, ...,X_n) = P(X_n|X_{n-1})$
		- the probability of being in a particular state $X_n$​ at time $n$ depends only on the state $X_{n−1}$​ at the previous time step, and not on any earlier states $X_0​,X_1​,…,X_{n−2​}$
		- Future only depends on the present
## Markov Chains ^n
- Raising a Markov chain's probability matrix to a power n means we are looking at it n steps ahead
	- Ex: 2 steps ahead, do $P^2$
## Irreducible Markov Chain
- It must be possible to reach any state from any other state in a finite number of steps
	- i.e. all states communicate
## Ergodic Chains
- it **forgets its starting state** and converges to a unique **stationary distribution** (or steady-state probabilities). 
	- In simpler terms, no matter where the chain starts, it eventually behaves in a predictable, long-term manner.
- For this to hold, you need to prove that:
	- It is **stationary in distribution**:
		- Find a row vector such that $\pi * P = \pi$
			- This means that the vector π doesn't change when multiplied by the transition matrix P. In other words, π is a stationary distribution.
		- Sum of all $\pi_i$ components must = 1
	- Also prove it is **irreducible**
	- Also prove it is **aperiodic**
		- Doesn't follow a concrete cycle (State 1 → State 2 → State 3 → State 1 → ...)
### Finding the row vector  $\pi * P = \pi$
- Example transition matrix:
	- $P = \begin{pmatrix} 0.5 & 0.5 & 0 \\ 0.25 & 0.5 & 0.25 \\ 0 & 0.5 & 0.5 \end{pmatrix}$
- Then fit $\pi * P = \pi$
	- $\pi_1 = 0.5 \pi_1 + 0.25 \pi_2$
	- $\pi_2 = 0.5 \pi_1 + 0.5 \pi_2 + 0.5 \pi_3$
	- $\pi_3 = 0.25 \pi_2 + 0.5 \pi_3$
	- $\pi_1 + \pi_2 + \pi_3 = 1$
#### Candidate Stationary Probabilities
- This refers to $\pi_1, \pi_2, \pi_3$ and the stationary condition $\pi_1 + \pi_2 + \pi_3 = 1$ 
## Expectation of a Markov Chain
- Example:
- $\mathbb{E}[X_2 \mid X_0 = 0] = \sum_{j} j \cdot P^2(0,j)$
	- Or $\mathbb{E}[X_2 \mid X_0 = 0] = 0 \cdot P^2(0,0) + 1 \cdot P^2(0,1) + 2 \cdot P^2(0,2)$
	- In words: expected value 2 steps ahead of the row corresponding to 0 (starting at row 0)
		- Row 0 is denoted by = 0. If it started at 1 it would equal 1 and so on...
- So with this matrix:
	- $P = \begin{pmatrix}\frac{1}{2} & \frac{1}{3} & \frac{1}{6} \\0 & \frac{1}{3} & \frac{2}{3} \\\frac{1}{2} & 0 & \frac{1}{2}\end{pmatrix}$
	- You'd get $P^2$ = 
		- $P^2 = \begin{pmatrix}\frac{1}{3} & \frac{5}{18} & \frac{11}{36} \\\frac{1}{3} & \frac{1}{9} & \frac{5}{9} \\\frac{1}{2} & \frac{1}{6} & \frac{1}{3}\end{pmatrix}$
			- Then you extract row and sub in the probabilities
				- $\mathbb{E}[X_2 \mid X_0 = 0] = 0 \cdot \frac{1}{3} + 1 \cdot \frac{5}{18} + 2 \cdot \frac{11}{36} = \frac{5}{18} + \frac{22}{36} = \frac{8}{9}$
- If asked $\mathbb{E}[X_2]$ without additional context
	- Calculate the weighted probability of the whole thing 2 steps ahead (or n if subscript is n)
## Random Walk with Markov Chains
- ![[Pasted image 20241022213703.png]]
- [[Geometric Random Walk]]
### Gamblers Ruin with Markov Chains
- Specific case of a Markov chain / random walk
- State 0 represents ruin (losing all money)
- State N represents success (win the game)
- Gambler stops playing at 0 or N
- "Probability of ruin in 1 step" --> probability of going to state 0 (usually from state 1)
- "Probability of ruin in X steps" --> raise the matrix to the power X and find $P_{1,0}$
## Misc
- $P(X_0 = 0) = P(X_0 = 1) = 1/4$
	- This basically means that the probability of the state starting at 0 or 1 is 1/4
	- This information is treated exogenously of expectation of something
	Example:
	- To compute the overall expected value $( \mathbb{E}[X_3] )$, we use the following steps:
		1. **Calculate the conditional expected value for each starting state**:
		   - $( \mathbb{E}[X_3 \mid X_0 = 0] )$: Use the first row of the matrix $( P^3)$.
		   - $( \mathbb{E}[X_3 \mid X_0 = 1] )$: Use the second row of the matrix $( P^3)$.
		   - $( \mathbb{E}[X_3 \mid X_0 = 2])$: Use the third row of the matrix $( P^3 )$.
		   
		2. **Multiply by the starting probabilities**:
		   - Multiply $( \mathbb{E}[X_3 \mid X_0 = 0] )$ by $(P(X_0 = 0) = \frac{1}{4} )$,
		   - Multiply $( \mathbb{E}[X_3 \mid X_0 = 1] )$ by $( P(X_0 = 1) = \frac{1}{4})$,
		   - Multiply $( \mathbb{E}[X_3 \mid X_0 = 2] )$ by $( P(X_0 = 2) = \frac{1}{2} )$.
   
		3. **Sum the weighted values**:
		   - Finally, sum the weighted expected values to get the overall expected value:
		   $\mathbb{E}[X_3] = \frac{1}{4} \cdot \mathbb{E}[X_3 \mid X_0 = 0] + \frac{1}{4} \cdot \mathbb{E}[X_3 \mid X_0 = 1] + \frac{1}{2} \cdot \mathbb{E}[X_3 \mid X_0 = 2$
