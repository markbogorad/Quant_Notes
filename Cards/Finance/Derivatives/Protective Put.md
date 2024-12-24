up:: [[Derivatives MOC]]
tags:: #Finance 
# Protective Put
- **Strategy:** Bullish with a hedge for downside protection (same chart as regular call)
	- Essentially reconstructing the long [[Call Option]] payoff, except you can retain stock ownership (for dividends, tax, voting)
- **Components:** 
	- Long underlying
	- Long [[Put Option]]
- **Payoff table:**

| Position             | Pay-Off                                                   |                            |
| -------------------- | --------------------------------------------------------- | -------------------------- |
|                      | $( S_T \leq K )$                                          | $( S_T > K )$              |
| Long Stock           | $( S_T )$                                                 | $( S_T )$                  |
| Long 1 Put @ \( K \) | $( K - S_T )$                                             | $( - \text{Premium} )$     |
| **Total Payoff**     | $( K - S_T + S_T - \text{Premium} = K - \text{Premium} )$ | $( S_T - \text{Premium} )$ |

- $( S_T \leq K )$ (Stock price at or below the strike price at expiration):
	- Exercise the put for downside protection -> loses on stock will match gains on put

-  $( S_T > K )$ (Stock price above the strike price at expiration):
	- Regular upside from a stock less the premium you paid for the put insurance

- **Profit graph:**

![[Pasted image 20240626100503.png]]