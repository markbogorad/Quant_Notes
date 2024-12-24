up:: [[Derivatives MOC]]
tags:: #Finance 
## Bull Call Spread
- **Strategy:** Bullish with a risk hedge for extreme changes
- **Components:** 
	- Long [[Call Option]] with low strike price ($K_1$)
	- Short [[Call Option]] with a higher strike price $(K_2)$
	- Key: choose tails properly by setting proper strike prices for $K_1$ and $K_2$
	- Key: Long and Short calls must have the same exact notional amount!
- **Payoff table:**

| Position                 |                   | Pay-Off                     |                   |
| ------------------------ | ----------------- | --------------------------- | ----------------- |
|                          | $( S_T \leq K_1)$ | $( K_1 \leq S_T \leq K_2 )$ | $( K_2 \leq S_T)$ |
| Long 1 Call @ $( K_1 )$  | 0                 | $( S_T - K_1 )$             | $( S_T - K_1 )$   |
| Short 1 Call @ $( K_2 )$ | 0                 | 0                           | $( K_2 - S_T )$   |
| Total                    | 0                 | $( S_T - K_1 )$             | $( K_2 - K_1 )$   |

- If below the lower strike price $K_1$ then neither $K_1$ nor $K_2$ will be exercised
	- Lose the premium on long call
	- Gain on the premium on the more extreme call (paid to you regardless but not exercised)
	- Profit is the loss on the net premium, which will be a loss because closer to the money options are worth more as there is a higher chance of exercising
- If in between  $K_1$ and $K_2$ 
	- Gain on long up until the exercise price of your short
	- Short call is still worthless, so you fain that premium
- If at or above $K_2$ -> **ideal!**
	- You will make a maximum of the gain on the long call until it reaches the price of $K_2$
		- After, any additional price increase, your gains on the call will have to match what you need to pay your short
			- Therefore, sizes must be 1:1

- **Profit graph:**

![[Pasted image 20240623223121.png]]


## Bull Put Spread
- **Strategy:** Bullish with a risk hedge for extreme changes, looking to pocket premiums (mirror of the bull call spread)
	- Engineered so that there is a capital inflow (via the net premium) on a bullish position
	- Risk is limited but this is still a risky strategy!
- **Components:** 
	- Long [[Put Option]] with low strike price ($K_1$) (ex: buy a put with strike $50)
	- Short [[Put Option]] with a higher strike price $(K_2)$ (ex: sell a put with strike $60)
	- Key: choose tails properly by setting proper strike prices for $K_1$ and $K_2$
	- Key: Long and Short calls must have the same exact notional amount!
- **Payoff table:**

| Position                |                    | Pay-Off                     |                    |
| ----------------------- | ------------------ | --------------------------- | ------------------ |
|                         | $( S_T \leq K_1 )$ | $( K_1 \leq S_T \leq K_2 )$ | $( K_2 \leq S_T )$ |
| Long 1 Put @ $( K_1 )$  | $( K_1 - S_T )$    | 0                           | 0                  |
| Short 1 Put @ $( K_2 )$ | $(- (K_2 - S_T) )$ | $(- (K_2 - S_T) )$          | 0                  |
| Total                   | $( K_1 - K_2 )$    | $( S_T - K_2 )$             | 0                  |

- If at or above $K_2$ - **ideal is at or above $K_2$**
	- Both puts expire worthless -> right to sell at a price below market is pointless
	- Earn the net premium received
- If in between $K_2$ and $K_1$ - lose money
	- $K_2$ is exercised against you
	- $K_1$ is out of the money and expires worthless
	- Net loss = $S_T - K_2 + \text{Net Premium}$
- If below $K_1$ - lose money
	- $K_2$ is deep in the money
	- $K_1$ will begin to cover the additional losses of $K_2$ below the strike of $K_1$


- **Profit graph:**

![[Pasted image 20240623225334.png]]

