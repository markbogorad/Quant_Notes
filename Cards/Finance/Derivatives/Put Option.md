up:: [[Derivatives MOC]]
tags:: #Finance
# Put Options
- **Long Put**
	- *Intuition:* you are looking to exploit the depreciation of the underlying and are purchasing the right to sell this at a higher price than it will be worth
	- This is still a bearish position
	- Gives the buyer the **right** but not the obligation to **sell** a stock at a specified price within a certain period of time
		- You essentially make money if the underlying goes down
- **Long Put Profit:** $= max[K-S, 0] - c$
	- S is the price of the underlying
	- K is the strike price
	- c is the put premium
	- If $S>K$
		- Underlying has appreciated beyond strike price, you lose the premium $(0-c)$
		- *Intuition:* you have the right to sell at a lower price than the market is offering to buy --> useless
	- If $S<K$ 
		- Underling has depreciated, making you in the money and you gain the difference 
		- Intuition: you have the right to sell at a price higher than the market is offering --> essentially forcing the counterparty to take your bad deal
	- ![[Pasted image 20240623203800.png]]



- **Short Put**
	- *Intuition:* you are the counterparty to the person looking to exploit the depreciation of the underlying. 
	- Bullish outlook
	- The seller (writer) grants the buyer the right, but not the obligation, to sell the underlying asset at a specified strike price within a certain period of time.
		- Seller receives option premium upfront
- **Short Put Profit:**$= c- max[K-S, 0]$
	- Either win premium or lose whatever additional price depreciation occurs beyond your expectations (limit to price = 0)
		- Same payoff structure as the call but bets on the underlying are inverse in terms of direction
	- If $S>K$
		- The underlying has surpassed the value of the agreed exercised price
		- Buyer (who was betting short) will **lose premium**
	- If $S<K$
		- The value of the underlying has dropped below the agreed upon price
		- You are open to losses until the stock goes to 0 theoretically
	- ![[Pasted image 20240623203817.png]]


## Put vs Holding Pure Stock Long:
### Same exact scenario as call except the bets are flipped
#### Capital Requirement
- **Long Put:** Less money upfront (only premium)
- **Short Put:** Income upfront via premium, may need margin to cover adverse moves however
- **Stock:** Requires you to buy full stock (usually way more than premium)
#### Risk
- **Long Put:** Risk is *limited* to losing the premium
- **Short Put:** Risk is *unlimited*, fully depends on the price movement of the underlying as the seller will *have to supply*
- **Stock:** Far less risky than options. If a stock moves 1-2% a day, an option might move 10-20% a day. However, the worst case for stocks is the entire asset (stock goes to 0) and is *limited*
#### Profit Potential
- **Long Put:** High profit potential due to **leverage**, small movements in underlying can lead to large movements in option
- **Short Put:** Limited to premium, no additional income no matter what
- **Stock:** Linear profit, no expiration allows for long term profits
#### Leverage
- **Long Put:** *High leverage* - exposure to large price movements of the underlying for a fraction of the cost
- **Short Put:** Income upfront via premium, theoretiPuty can be reinvested and is leverage but small
- **Stock:** No leverage
#### Time Sensitivity
- **Long Put:** Bad side of exponential time decay as expiration approaches, especially if not in the money
- **Short Put:** Good side of exponential decay - value of option usually decreases over time
- **Stock:** Requires you to buy full stock (usually way more than premium)