up:: [[Stochastic Calculus MOC]]
tags:: #Math 
# Key Differences in Wording

| **Characteristic**         | **Random Walk**               | **Brownian Motion**                          | **Arithmetic Process**               | **Geometric Process**                      |
| -------------------------- | ----------------------------- | -------------------------------------------- | ------------------------------------ | ------------------------------------------ |
| **Time Index**             | **Discrete**                  | **Continuous**                               | Can be either discrete or continuous | Can be either discrete or continuous       |
| **Definition**             | $S_n=S_n−1+X_n$​              | $W_t∼N(0,t)$                                 | $S_n=S_n−1+X_n$​                     | $S_n=S_n−1⋅(1+X_n)$                        |
| **Increments**             | Additive: $X_i∈{−1,+1}$       | Additive: $Wt−Ws∼N(0,t−s)$                   | Additive: $S_n=S_n−1+X_n$​           | Multiplicative: $S_n=S_n−1⋅(1+X_n)$        |
| **Increment Distribution** | Typically Bernoulli           | Normal                                       | Typically normal                     | Typically normal                           |
| **Common Application**     | Simple models of stock prices | Modeling physical phenomena and stock prices | Modeling absolute changes or returns | Modeling stock prices and relative changes |
| **Path Properties**        | Discrete steps                | Continuous paths                             | Discrete or continuous steps         | Discrete or continuous steps               |
| **Mathematical Form**      | $S_n=S_n−1+X_n$​              | $dX_t=μdt+σdW_t$​                            | $S_n=S_n−1+X_n$​                     | $dS_t=μS_tdt+σS_tdW_t$​                    |
| **Example Formula**        | $S_n=∑_{i=1}^nX_i$​           | $W_t∼N(0,t)$                                 | $S_n=S_n−1+X_n$​                     | $S_t=S_0exp⁡((μ−σ22)t+σW_t)$               |
| **Nature of Process**      | Additive                      | Additive                                     | **Additive**                         | **Exponential**                            |
