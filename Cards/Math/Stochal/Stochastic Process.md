up:: [[Stochastic Calculus MOC]]
tags:: #Math
# Stochastic Process
- A stochastic process is **a collection of random variables** indexed by time or another variable, *representing a system that evolves over time in a way that is not deterministic.*

### Types of Stochastic Processes
-  **Discrete-time Stochastic Process**: 
    Example: A [[Geometric Random Walk]]
    
- **Continuous-time Stochastic Process**: 
    Example: [[Geometric Brownian Motion]]

### Key Properties
- **State Space**: The set of all possible values that the random variables $X_t$​ can take.
- **Stationarity**: A stochastic process ${X_t​}$ is said to be stationary if the joint distribution of $(X_{t_1},X_{t_2},…,X_{t_n})$ is invariant under time shift.
- **Markov Property**: A process ${X_t​}$ has the Markov property if the future state $Xt+1​$ depends only on the present state $X_t$​ and not on past states. [[Markov Switching Models]]
- **Independence**: Increments of the process $X_t+s​−X_t$​ are independent of $X_t$​.
