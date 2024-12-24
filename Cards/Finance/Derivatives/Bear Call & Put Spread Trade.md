up:: [[Derivatives MOC]]
tags:: #Finance 
## Bear Call Spread
- **Strategy:** Bearish with a risk hedge for extreme changes: profit off moderate to slight decline
	- Think of this as the bearish version of the bull put spread [[Bull Call & Put Spread Trade]]
	- Looking to **pocket the premium** in a hedged way
	- Generates a net cash inflow via the premia recieved
- **Components:** 
	- Short [[Call Option]] with low strike price ($K_1$) (sell call)
	- Long [[Call Option]] with a higher strike price $(K_2)$
	- Key: choose tails properly by setting proper strike prices for $K_1$ and $K_2$
	- Key: Long and Short calls must have the same exact notional amount!
- **Payoff table:**

| Position              |                   | Pay-Off                   |                   |
| --------------------- | ----------------- | ------------------------- | ----------------- |
|                       | $( S_T \leq K1 )$ | $( K1 \leq S_T \leq K2 )$ | $( K2 \leq S_T )$ |
| **Short 1 Call @ K1** | 0                 | $(K1 - S_T)$              | $(K1 - S_T)$      |
| **Long 1 Call @ K2**  | 0                 | 0                         | \(S_T - K2\)      |
| **Total**             | 0                 | $(K1 - S_T)$              | $(K1 - K2)$       |

- If below $K_1$: **ideal**
	- Both options expire worthless, win the premium
- If in between $K_1$ and $K_2$:
	- Long call ($K_2$) expires worthless -> didn't reach the necessary strike price
	- Short call takes a loss as price appreciates above $K_1$
	- Depending on premium size, this scenario can break even or lose money
- If above $K_2$
	- Long call activates -> matches further losses from the short call
- **Profit graph:**

![[Pasted image 20240624110448.png]]
- 
## Bear Put Spread
- **Strategy:** Bearish with a risk hedge for extreme changes
- **Components:** 
	- Short [[Put Option]] with low strike price ($K_1$) (sell put)
	- Long [[Put Option]] with a higher strike price $(K_2)$
- **Payoff table:**

| Position             |                   | Pay-Off                   |                   |
| -------------------- | ----------------- | ------------------------- | ----------------- |
|                      | $( S_T \leq K2 )$ | $( K2 \leq S_T \leq K1 )$ | $( K1 \leq S_T )$ |
| **Short 1 Put @ K1** | $( -(K1 - S_T))$  | $( -(K1 - S_T))$          | 0                 |
| **Long 1 Put @ K2**  | $(K2 - S_T)$      | $(K2 - S_T)$              | 0                 |
| **Total**            | $( K1 - K2 )$     | $( K1 - K2 )$             | 0                 |

- If below $K_1$: **ideal**
	- $K_1$ will be in the money and be exercised against you
	- $K_2$ will be in the money and generate income
	- All price points beyond $K_2$ will be profitless as $K_1$ will take them away
- If in between $K_1$ and $K_2$:
	- $K_1$ will incur a loss -> everything above the $K_1$ price will be a loss
	- $K_2$ will generate a profit --> everything below $K_2$ price makes money
	- Will be $K_1-K_2 -\text{Net Premium}$
- If above $K_2$
	- Both options expire worthless
	- Lose net premium

**Profit graph:**

![[Pasted image 20240624110429.png]]






