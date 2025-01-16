up:: [[Oil Markets MOC]]
tags:: #Finance 
# Value
- [[Algorithmic Trading in Oil]]
- A [[Mean Reversion Process (Ornstein-Uhlenbeck)]] strategy
- Not practically viable due to headwinds of negative carry
- The exact opposite of [[Oil Momentum Risk Premia]]
## Estimating Fair Value
- Very hard in practice
- Common method: statistical definition that is essentially reverse of [[Oil Momentum Risk Premia]] using [[MA]]s
$$\pi_v(F_t)=-\pi_M(F_t)=-sign(M_t(n))$$
- Buy futures when price falls below MA
- Sell futures when price rises above MA
## Common Additions to Strategy
- Use a threshold to only enter when deviation is significant enough