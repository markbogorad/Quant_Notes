up:: [[Derivatives MOC]]
tags:: #Finance 
# Covered Call
- **Strategy:** Bullish but not overly with a hedge for your long stock position with a short call 
- **Components:** 
	- Own the underlying (long)
	- Short [[Call Option]]
- **Payoff table:**

| Position               | Pay-Off                    |                                    |
| ---------------------- | -------------------------- | ---------------------------------- |
|                        | $( S_T \leq K )$           | $( S_T > K )$                      |
| Long Stock             | $( S_T )$                  | $( S_T )$                          |
| Short 1 Call @ \( K \) | $( + \text{Premium} )$     | $( + \text{Premium} - (S_T - K) )$ |
| **Total Payoff**       | $( S_T + \text{Premium} )$ | $( K + \text{Premium} )$           |

- $( S_T \leq K )$ (Stock price at or below the strike price at expiration):
	- Call will go unexercised
	- Total gain is the stock appreciation plus the premium paid by selling the short call

- $( S_T > K )$ (Stock price above the strike price at expiration):
   - Short call gets exercised against you
   - Strike price becomes the ceiling of your maximum profit, as losses on the short call will offset the underlying position

- **Profit graph:**

![[Pasted image 20240626095950.png]]