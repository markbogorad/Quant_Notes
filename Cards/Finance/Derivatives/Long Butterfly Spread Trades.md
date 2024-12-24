up:: [[Derivatives MOC]]
tags:: #Finance 
# Long Butterfly Spread
- A bet on **low volatility** 
- Essentially a combination of [[Bull Call & Put Spread Trade]] and [[Bear Call & Put Spread Trade]]
- Key differences are highlighted in [[Butterfly Spread Trades]]
## Long Butterfly Spread with Calls
- **Strategy:** 
	- Profit from low volatility in underlying (slightly bullish)
- **Components:** 
	- Long 1 [[Call Option]] at a lower strike $K_1$
	- Short 2 [[Call Option]] at a middle strike price $K_2$
	- Long 1 [[Call Option]] at a higher strike price $K_3$
	- The strike prices are such that $K1<K2<K3$ and the distance between is equal ($K2−K1=K3−K2$).
		- Ex: 50 - 60 -70
	- Net premium is typically 0: cost of long calls is negated by profit off shorts for premium only
	
- **Payoff table:**

| Position                  |                   | Pay-Off                      |                                           |                    |
| ------------------------- | ----------------- | ---------------------------- | ----------------------------------------- | ------------------ |
|                           | $( S_T \leq K1 )$ | $( K1 \leq S_T \leq K2 )$    | $( K2 \leq S_T \leq K3 )$                 | $( S_T \geq K3 )$  |
| Long 1 Call at \( K1 \)   | 0                 | $( S_T - K1 )$               | $( S_T - K1 )$                            | $( S_T - K1 )$     |
| Short 2 Calls at \( K2 \) | 0                 | $( -2(S_T - K2) )$           | $( -2(S_T - K2) )$                        | $( -2(S_T - K2) )$ |
| Long 1 Call at \( K3 \)   | 0                 | 0                            | $( S_T - K3 )$                            | $( S_T - K3 )$     |
| **Total**                 | 0                 | $( S_T - K1 - 2(S_T - K2) )$ | $( S_T - K1 - 2(S_T - K2) + (S_T - K3) )$ | 0                  |


- **Profit graph:**
![[Pasted image 20240624154612.png]]



## Long Butterfly Spread with Puts
- **Strategy:** 
	- A bet on **low volatility** but slightly **bearish** as they expect the option price to fall to $K_2$
	- Essentially a combination of [[Bull Call & Put Spread Trade]] and [[Bear Call & Put Spread Trade]]
- **Components:** 
	- Long 1 [[Put Option]] at a lower strike $K_1$
	- Short 2 [[Put Option]] at a middle strike price $K_2$
	- Long 1 [[Put Option]] at a higher strike price $K_3$
	- The strike prices are such that $K1<K2<K3$ and the distance between is equal ($K2−K1=K3−K2$).
	
- **Payoff table:**

| Position                 |                                           | Pay-Off                   |                              |                   |
| ------------------------ | ----------------------------------------- | ------------------------- | ---------------------------- | ----------------- |
|                          | $( S_T \leq K1 )$                         | $( K1 \leq S_T \leq K2 )$ | $( K2 \leq S_T \leq K3 )$    | $( S_T \geq K3 )$ |
| Long 1 Put at \( K3 \)   | $( K3 - S_T )$                            | $( K3 - S_T )$            | $( K3 - S_T )$               | 0                 |
| Short 2 Puts at \( K2 \) | $( -2(K2 - S_T) )$                        | $( -2(K2 - S_T) )$        | 0                            | 0                 |
| Long 1 Put at \( K1 \)   | $( K1 - S_T )$                            | 0                         | 0                            | 0                 |
| **Total**                | $( K3 - S_T - 2(K2 - S_T) + (K1 - S_T) )$ | 0                         | $( K3 - S_T - 2(K2 - S_T) )$ | 0                 |


- **Profit graph:**
![[Pasted image 20240624154612.png]]
- Same exact graph as long butterfly with calls