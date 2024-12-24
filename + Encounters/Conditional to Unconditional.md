up:: [[Probability MOC]]
tags:: #Math 
# Going from conditional to unconditional
- Assume that we repeatedly throw a die until the first time that we get a6for the first time. What is the expected number of 1s that we throw given that we see a 6 for the first time in the kth throw

### Step-by-Step Solution:

#### Step 1: Conditional Expectation
Given that the first 6 appears on the \( k \)-th throw, the expected number of 1s thrown up to and including the \( k \)-th trial is as follows:

- For each throw, the probability of getting a 1 is $( \frac{1}{6} )$.
- Therefore, the expected number of 1s in $( k-1 )$ throws (since the \( k \)-th throw is a 6) is $( \frac{k-1}{6}$).

So, the conditional expectation is:

$\mathbb{E}[Y_k | \text{first 6 at } k] = \frac{k-1}{6}$

#### Step 2: Unconditional Expectation
Now, to find the unconditional expectation, you sum over all possible values of \( k \), weighted by the probability that the first 6 occurs on the \( k \)-th throw.

The probability that the first 6 occurs on the \( k \)-th throw is \( \left(\frac{5}{6}\right)^{k-1} \cdot \frac{1}{6} \).

Therefore, the unconditional expectation of the number of 1s is:

\[
\mathbb{E}[Y_k] = \sum_{k=1}^{\infty} \mathbb{E}[Y_k | \text{first 6 at } k] \cdot P(\text{first 6 at } k)
\]

Substituting the values:

\[
\mathbb{E}[Y_k] = \sum_{k=1}^{\infty} \frac{k-1}{6} \cdot \left(\frac{5}{6}\right)^{k-1} \cdot \frac{1}{6}
\]

Simplifying further:

\[
\mathbb{E}[Y_k] = \frac{1}{36} \sum_{k=1}^{\infty} (k-1) \left(\frac{5}{6}\right)^{k-1}
\]

#### Step 3: Solve the Series
The sum \( \sum_{k=1}^{\infty} (k-1) x^{k-1} \) for \( x = \frac{5}{6} \) can be computed using the formula for the sum of a geometric series and its derivative:

\[
\sum_{k=1}^{\infty} (k-1) x^{k-1} = \frac{x}{(1-x)^2}
\]

For \( x = \frac{5}{6} \):

\[
\sum_{k=1}^{\infty} (k-1) \left(\frac{5}{6}\right)^{k-1} = \frac{\frac{5}{6}}{\left(\frac{1}{6}\right)^2} = 30
\]

#### Final Answer:
\[
\mathbb{E}[Y_k] = \frac{1}{36} \times 30 = \frac{5}{6}
\]

So, the unconditional expectation of the number of 1s thrown before getting a 6 is \( \frac{5}{6} \).