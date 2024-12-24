up:: [[Derivatives MOC]]
tags:: #Finance 
# Call Options
- **Long Call**
	- Gives the buyer the right, but not the obligation, to purchase a stock at a specified price (the strike price) within a certain period of time.
	- **Long Call Profit**: $= max[S-K, 0] - c$
		- S is underlying price
		- k is the strike price (exercise price)
		- c is the premium on the call
		- If $S>K$
			- Option worth more than agreed price and will be exercised
			- Profit = $S-K$
		- If $S<K$
			- Option worth less than agreed and wont be exercised
			- Loss = c
	- ![[Pasted image 20240623195220.png]]



- **Short Call (selling the call)**
	- The writer grants the buyer the right, but not the obligation, to buy the underlying asset at a specified strike price within a certain period of time.
		- Seller receives option premium upfront for this
	- **Short Call Profit: = $c- max[S-K, 0]$**
		- The premium here is your maximum payment
		- Either win premium or lose whatever you need to pay up to match future stock price (will need to deliver the stock later)
			- Theoretically infinite loss
		- If $S>K$
			- The underlying has surpassed the value of the agreed exercised price --> *buyer will want to exercise*
		- If $S<K$
			- The value of the underlying has dropped below the agreed upon price --> *you win the premium (c)*
	- ![[Pasted image 20240623195232.png]]


## Call vs Holding Pure Stock Long:
#### Capital Requirement
- **Long Call:** Less money upfront (only premium)
- **Short Call:** Income upfront via premium, may need margin to cover adverse moves however
- **Stock:** Requires you to buy full stock (usually way more than premium)
#### Risk
- **Long Call:** Risk is *limited* to losing the premium
- **Short Call:** Risk is *unlimited*, fully depends on the price movement of the underlying as the seller will *have to supply*
- **Stock:** Far less risky than options. If a stock moves 1-2% a day, an option might move 10-20% a day. However, the worst case for stocks is the entire asset (stock goes to 0) and is *limited*
#### Profit Potential
- **Long Call:** High profit potential due to **leverage**, small movements in underlying can lead to large movements in option
- **Short Call:** Limited to premium, no additional income no matter what
- **Stock:** Linear profit, no expiration allows for long term profits
#### Leverage
- **Long Call:** *High leverage* - exposure to large price movements of the underlying for a fraction of the cost
- **Short Call:** Income upfront via premium, theoretically can be reinvested and is leverage but small
- **Stock:** No leverage
#### Time Sensitivity
- **Long Call:** Bad side of exponential time decay as expiration approaches, especially if not in the money
- **Short Call:** Good side of exponential decay - value of option usually decreases over time
- **Stock:** Requires you to buy full stock (usually way more than premium)