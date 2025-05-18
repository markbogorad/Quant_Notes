up:: [[Time Series MOC]]
tags:: #Machine_Learning 
# Markov Switching Models
**Intuition**: This model assumes that the time series **alternates between distinct regimes** (e.g., high and low volatility) according to a Markov process. The transition probabilities between regimes are estimated, making it ideal for capturing regime changes driven by unobserved factors.
$$y_t = \mu_{S_t} + \phi_{S_t} y_{t-1} + \varepsilon_t$$
- Evolves according to a hidden Markov process and transition is based off it's [[Markov Chains]]
- Actual algorithm uses the [[Maximum Likelihood Estimator]] to maximize the likelihood of observing states via [[Gradient Descent]]