up:: [[Probability MOC]]
tags:: #Math
# Joint Distributions
- **Joint distributions** describe the probability distribution of *two or more random variables taken together*. They provide a complete picture of how the variables interact with each other.
	- This is modeled in a Joint Random Vector -> vector of variables describing joint behavior
## Discrete
- Probability that a [[Random Variables]] **takes on a value simultaneously** with something else
### Discrete Joint [[Probability Mass Function (PMF)]]
$$p_{X,Y}(x,y) = P(X = x \text{ and } Y = y)$$
- For two discrete random variables $X$ and $Y$, the joint PMF is denoted as $pX,Y​(x,y)$, and it gives the probability that $X=x$ and $Y=y$  occur together.
### Discrete Joint [[Cumulative Distribution Function (CDF)]]
$$F_{X,Y}(x,y) = \sum_{x' \leq x} \sum_{y' \leq y} p_{X,Y}(x', y')$$
### Expectation
$$E[g(X, Y)] = \sum_{x} \sum_{y} g(x, y) \cdot p_{X,Y}(x, y)$$
## Joint Continuous Variables
- The likelihood of the variables **falling within a specific range simultaneously**.
### Joint [[Probability Density Function (PDF)]]
$$P(a \leq X \leq b, c \leq Y \leq d) = \int_{a}^{b} \int_{c}^{d} f_{X,Y}(x,y) \, dx \, dy$$
### Continuous Joint [[Cumulative Distribution Function (CDF)]]
$$F_{X,Y}(x,y) = \int_{-\infty}^{x} \int_{-\infty}^{y} f_{X,Y}(x', y') \, dy' \, dx'
$$

### Expectation
$$E[g(X, Y)] = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty} g(x, y) \cdot f_{X,Y}(x, y) \, dx \, dy$$

## Example
This example involves two fair dice \( X \) and \( Y \), and a new random variable \( M \), which represents the maximum of the two dice rolls: $( M = \text{max}(X, Y) )$. The problem asks for the probability of different events involving \( X \) and \( M \).

### Key Concepts:

- **\( X \) and \( Y \)** are the outcomes of rolling two fair dice, so each can take a value from 1 to 6.
- **\( M = \text{max}(X, Y) \)** means that \( M \) takes the maximum value between the two rolls.

### Questions and Answers:

1. **What is the probability that \( X = 5 \) and \( M = 6 \)?**
   - **Interpretation**: If \( M = 6 \), this means that the maximum value between $( X )$ and $( Y )$ must be 6. Given $( X = 5 )$, the only way $( M )$ can equal 6 is if $( Y = 6 )$.
   - **Calculation**: The probability that $( X = 5 )$ and $( Y = 6 )$ is the product of the probabilities of these independent events, which is $( \frac{1}{6} \times \frac{1}{6} = \frac{1}{36} )$.

   $P(X = 5, M = 6) = P(X = 5, Y = 6) = \frac{1}{36}$

2. **What is the probability that \( X = 5 \) and \( M = 3 \)?**
   - **Interpretation**: If \( M = 3 \), the maximum value between \( X \) and \( Y \) is 3. However, if \( X = 5 \), then the maximum value cannot be 3 (because 5 is greater than 3).
   - **Conclusion**: This event is impossible, so the probability is 0.
   
   $P(X = 5, M = 3) = 0$

3. **What is the probability that \( X = 5 \) and \( M = 5 \)?**
   - **Interpretation**: For \( M = 5 \), the maximum of the two dice rolls must be 5. Given \( X = 5 \), \( Y \) must be 5 or less for the maximum to still be 5.
   - **Calculation**: The probability that \( X = 5 \) and \( Y \leq 5 \) involves \( Y \) taking any of the values 1, 2, 3, 4, or 5. Each of these outcomes has a probability of $( \frac{1}{6} )$, and there are 5 possible outcomes. The probability is then:

   $P(X = 5, M = 5) = P(X = 5, Y \leq 5) = \frac{1}{6} \times \frac{5}{6} = \frac{5}{36}$
### Summary:

- **First Case**: \( X = 5 \) and \( M = 6 \) is possible only if \( Y = 6 \), so the probability is $( \frac{1}{36} )$.
- **Second Case**: \( X = 5 \) and \( M = 3 \) is impossible, so the probability is 0.
- **Third Case**: \( X = 5 \) and \( M = 5 \) is possible if $( Y \leq 5 )$, so the probability is $( \frac{5}{36} )$.

This example illustrates how to calculate joint probabilities involving the maximum of two random variables, considering different conditions and the relationships between the variables.