up:: [[Derivatives MOC]]
tags:: #Finance 
# Straddle Trade
- These are bets on volatility
	- Long straddle --> high volatility
	- Short straddle --> low volatility, same as [[Butterfly Spread Trades]]
- Useful in [[Mergers & Acquisitions]] arbitrage
## Long Straddle
- **Strategy:** Pure bet on volatility -> both bullish and bearish
- **Components:** 
	- Long [[Call Option]] at strike $K$
	- Long [[Put Option]] at same strike $K$
- **Payoff table:**

| Position              | $( S_T \leq K )$ | $( S_T \geq K )$ |
| --------------------- | ---------------- | ---------------- |
| Buy 1 Call at \( K \) | 0                | $( S_T - K )$    |
| Buy 1 Put at \( K \)  | $( K - S_T )$    | 0                |
| **Total**             | $( K - S_T )$    | $( S_T - K )$    |

- **Profit graph:**

![[Pasted image 20240626161713.png]]



## Short Straddle
- **Strategy:** Low volatility play, very similar to [[Butterfly Spread Trades]]
- **Components:** 
	- Short [[Call Option]] at strike $K$
	- Short [[Put Option]] at same strike $K$
- **Payoff table:**

| Position               | $( S_T \leq K )$ | $( S_T \geq K )$ |
| ---------------------- | ---------------- | ---------------- |
| Sell 1 Call at \( K \) | 0                | $( -(S_T - K) )$ |
| Sell 1 Put at \( K \)  | $( -(K - S_T) )$ | 0                |
| **Total**              | $( -(K - S_T) )$ | $( -(S_T - K) )$ |

- **Profit graph:**

![[Pasted image 20240626161702.png]]

### Key Differences: Short Straddle vs. Butterfly Spread

| Feature                | Short Straddle                        | Butterfly Spread                                            |
| ---------------------- | ------------------------------------- | ----------------------------------------------------------- |
| **Construction**       | - Sell 1 call at \( K \)              | - Buy 1 call at \( K1 \)                                    |
|                        | - Sell 1 put at \( K \)               | - Sell 2 calls at \( K2 \)                                  |
|                        |                                       | - Buy 1 call at \( K3 \)                                    |
| **Profit Potential**   | - Limited to premiums received        | - Limited to difference between strikes minus net debit     |
| **Loss Potential**     | - Unlimited                           | - Limited to net debit paid                                 |
| **Breakeven Points**   | - $( K \pm \text{premium received} )$ | - $( K1 + \text{net debit} ) and ( K3 - \text{net debit} )$ |
| **Market Expectation** | - Low volatility                      | - Low volatility with range-bound price                     |
| **Risk/Reward**        | - High risk, limited reward           | - Limited risk, limited reward                              |
| **When to Use**        | - Expecting minimal price movement    | - Expecting price to stay within a narrow range             |
