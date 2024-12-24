up:: [[Probability MOC]]
tags:: #Math 
# Convolution
- Finding the distribution of [[Sums of Random Variables]]
- Summing multiple distributions to get their unique combination
$$F_n(x) = \int_{-\infty}^{+\infty} F(x - y) f_{n-1}(y) \, dy$$
- When you have two independent random variables X and Y, and you want to find the [[Probability Density Function (PDF)]] **of their sum** Z=X+Y, you use convolution.
- Fn​(x):
    - This represents the probability distribution (or a related function) of the sum of n independent random variables.
    - [[Cumulative Distribution Function (CDF)]]
- F(x−y):
    - Imagine you're shifting the function F(x) by an amount y. This shift accounts for all the different ways that two random variables can combine to form a particular outcome.
- fn−1​(y):
    - This is the probability density of the sum of the first n−1 random variables. Essentially, it tells you the probability of all the possible sums of those variables.
    - [[Probability Density Function (PDF)]]
## Intuition
- Convolution tells us how likely different outcomes are when we combine the results of these variables.
- Imagine you’re adding up n different things, like rolling n dice and adding the results. Each dice roll has its own probability distribution (which numbers you can roll and how likely they are). *The formula is a way to combine all these distributions together to figure out the probabilities of all possible sums you can get when you roll all n dice.*
- *The formula works by:*
- Taking the distribution of one of the random variables (like the result from one die roll) and shifting it around by all possible amounts (like adjusting for what the other dice might roll).
- Then it checks how these shifts overlap with the distribution of the sums of the previous dice rolls (or variables).
- Finally, it adds up all these overlaps to give you the new distribution for the sum of all n dice rolls.
## Derivative of Convolution
