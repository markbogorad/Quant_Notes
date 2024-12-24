up:: [[Probability MOC]]
tags:: #Math 
# Convergence Concepts
## Almost Sure (a.s)
- Very hard to prove (impractical) --> never really works
	- Often better to prove by [[Law of Large Numbers]] under the [[Poisson Distribution]] (poisson process)
$$P\left( \left\{ \omega : \lim_{n \to +\infty} X_n(\omega) = X(\omega) \right\} \right) = 1$$
- $X_n \to X$ almost surely as $n \to +\infty$ if and only if the set $N = \left\{ \omega : \lim_{n \to +\infty} X_n(\omega) \neq X(\omega) \right\}$ has probability 0, 
	- i.e., $[ P(N) = 0]$
- The more predictions you have the closer you get to the actual thing you are predicting
	- Literally [[Law of Large Numbers]] without [[I.I.D]] condition 
#### Proving:
- **So to solve these would be to use law of large numbers but prove elements are IID before**


## In Probability (in prob)
$$\lim_{n \to +\infty} P\left(\left\{ \omega : |X_n(\omega) - X(\omega)| > \epsilon \right\}\right) = 0, \quad \text{for every } \epsilon > 0$$
- A sequence of random variables $( X_n )$ is said to $\textit{converge in probability}$ to a random variable $( X )$ as $( n \to \infty )$ if, for every $( \epsilon > 0 )$, $\lim_{n \to \infty} P(|X_n - X| > \epsilon) = 0$ 
- This means that as $( n )$ increases, the probability that $( X_n )$ differs from $( X )$ by more than $( \epsilon )$ approaches zero.
	- Basically the error of difference will get smaller with more samples
#### Proving:
- **Goal**: Show that $\lim_{n \to +\infty}P(∣Xn−X∣>ϵ)=0$ for any $e > 0$
- **Steps**:
    1. Start by setting up $P(∣Xn​−X∣>ϵ)$
    2. Use properties of the distribution (such as the [[Cumulative Distribution Function (CDF)]]) or inequalities (like Markov's or [[Chebyshev's Inequality]]) to estimate or bound this probability.
    3. Take the limit as n→∞n→∞.
    4. If this limit is zero for all >0, then Xn​→X in probability.
- **Tip**: For sequences like minima or maxima *calculate the probability that Xn​ differs from X by more than ϵ* and analyze the limit directly.


## In Mean Squares (m.s)
$$\text{If } \mathbb{E}(|X_n|^2) < +\infty \text{ for all } n, \quad \mathbb{E}(|X|^2) < +\infty, $$ AND
$$\lim_{n \to \infty} \mathbb{E}[(X_n - X)^2] = 0$$
- This just basically says that MSE will decrease as sample size increase
	- This implies convergence in prob
#### Proving:
- **Goal**: Show that $\lim_{n \to \infty}E[(Xn−X)^2]=0$
- **Steps**:
    1. Calculate $E[(Xn−X)^2]$
    2. Use algebraic manipulations or bounds (like the [[Cauchy-Schwarz Inequality]]) to simplify or estimate this expectation.
    3. Take the limit as n→∞n→∞ and verify if it equals zero.


## In Distribution (in dis)
- AKA weak convergence
$$\lim_{n \to \infty} F_{X_n}(t) = F_X(t)$$
- Convergence in distribution means that the "shape" of the distribution of $X_n$​ becomes more similar to the distribution of $X$ as $n$ increases. However, it does not require $X_n$​ to get close to $X$ for individual values — it’s only about their distributions matching in the limit.
#### Proving:
- **Goal**: Show that $\lim_{n \to \infty}F_{X_n}(t)=F_X(t)$ for all continuity points $t$ of $F_X$​.
- **Steps**:
    1. Identify the cumulative distribution functions [[Cumulative Distribution Function (CDF)]] $F_{X_n}​$ and $F_X$​
    2. Check the limit $\lim_{n \to \infty} F_{X_n}(t)$ at points $t$ where $F_X$​ is continuous.
    3. If this limit matches $F_X​(t)$ for all such points, then $X_n→X$ in distribution.
- **Tip**: Convergence in distribution does not require $X_n$​ to get close to $X$ directly, just that the CDFs match in the limit. This is useful in cases like the [[Central Limit Theorem]]


# Hierarchy
$X_n \to X \text{ almost surely} \text{  AND  } X_n \to X \text{ in mean square} \Rightarrow X_n \to X \text{ in probability} \Rightarrow X_n \to X \text{ in distribution}.$

![[Screenshot 2024-10-25 at 1.12.15 PM.png]]