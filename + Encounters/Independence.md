up:: [[Probability MOC]]
tags:: #Math
# Independence
- **Independence** is a fundamental concept in probability and statistics that describes a situation where the occurrence or outcome of one event or random variable does not affect the occurrence or outcome of another event or random variable. When two events or random variables are independent, the knowledge of one provides no information about the other.
- [[Correlation]]
	- Independent variables are always uncorrelated (correlation = 0)
	- Uncorrelated variables are NOT always correlated
### Independence of Events
- Two events $( A )$ and $( B )$ are said to be independent if the probability of their intersection (both events happening together) is equal to the product of their individual probabilities. Mathematically:
	$P(A \cap B) = P(A) \times P(B)$

#### Interpretation:
- **If \( A \) and \( B \) are independent**, knowing that event \( A \) has occurred does not change the probability of event \( B \) occurring.
- **Example**: Suppose you flip a coin and roll a die. The event \( A \) (getting heads on the coin flip) and the event \( B \) (rolling a 6 on the die) are independent, because the outcome of the coin flip does not affect the outcome of the die roll:

### Independence of Random Variables
- Two random variables \( X \) and \( Y \) are independent if the joint probability distribution (or joint probability density function, in the continuous case) is equal to the product of their marginal distributions. Mathematically:

- **For discrete random variables**:
  $P(X = x \text{ and } Y = y) = P(X = x) \times P(Y = y)$

- **For continuous random variables**:
  $f_{X,Y}(x, y) = f_X(x) \times f_Y(y)$
  
#### Interpretation:
- **If \( X \) and \( Y \) are independent**, knowing the value of \( X \) does not change the probability distribution of \( Y \), and vice versa.
- **Example**: Suppose \( X \) is the number rolled on a die and \( Y \) is the outcome of a coin flip, coded as 0 for tails and 1 for heads. The distribution of \( X \) (a uniform distribution over 1 to 6) is independent of the distribution of \( Y \) (a Bernoulli distribution with parameter \( p = 0.5 \)).

### Testing for Independence

- **Independence of Events**: To test whether two events \( A \) and \( B \) are independent, you can check if \( P(A \cap B) = P(A)P(B) \). If equality holds, they are independent; otherwise, they are dependent.
  
- **Independence of Random Variables**: For random variables, independence is often tested by examining their joint distribution and comparing it to the product of their marginal distributions.


Two events A and B are independent if P(A|B) = P(A)


For continuous time --> marginal density functions --> joint dist must be product of marginal density functions