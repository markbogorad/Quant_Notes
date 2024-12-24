up:: [[Derivatives MOC]]
tags:: #Finance 
# Strangle Trade
- Bets on volatility but giving it more room than the [[Straddle Trade]]
	- Long straddle --> high volatility
	- Short straddle --> low volatility
## Long Strangle
- **Strategy:** Bet on volatility increasing with a wider band for movements (a less risky straddle)
- **Components:** 
	- Long [[Put Option]] at lower strike $K_1$
	- Long [[Call Option]] at higher strike $K_2$
- **Payoff table:**

| Position               | $( S_T \leq K1 )$ | $( K1 \leq S_T \leq K2 )$ | $( S_T \geq K2 )$ |
| ---------------------- | ----------------- | ------------------------- | ----------------- |
| Buy 1 Call at \( K2 \) | 0                 | 0                         | $( S_T - K2 )$    |
| Buy 1 Put at \( K1 \)  | $( K1 - S_T )$    | 0                         | 0                 |
| **Total**              | $( K1 - S_T )$    | 0                         | $( S_T - K2 )$    |

- **Profit graph:**

![[Pasted image 20240626163023.png]]



## Short Strangle
- **Strategy:** Bet on low volatility and minimal price movement within the rang $K_1$ to $K_2$
- **Components:** 
	- Short [[Put Option]] at lower strike $K_1$
	- Short [[Call Option]] at higher strike $K_2$
- **Payoff table:**

| Position                | $( S_T \leq K1 )$ | $( K1 \leq S_T \leq K2 )$ | $( S_T \geq K2 )$ |
| ----------------------- | ----------------- | ------------------------- | ----------------- |
| Sell 1 Call at \( K2 \) | 0                 | 0                         | \( -(S_T - K2) \) |
| Sell 1 Put at \( K1 \)  | $( -(K1 - S_T) )$ | 0                         | 0                 |
| **Total**               | $( -(K1 - S_T) )$ | 0                         | $( -(S_T - K2) )$ |

- **Profit graph:**

![[Pasted image 20240626163030.png]]