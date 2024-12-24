up:: [[Derivatives MOC]]
tags:: #Finance 
# Trading Ladder
- This is how futures traders trade, similar to [[Option Chain Quotes]] and level 2 for stocks

![[ladder.png]]

- BidQty -> bid quantity 
	- Best bid in red
- AskQty -> ask quantity
	- Best offer just above red = 384.00 on 515 contracts
- Fair value from a [[Market Makers]] perspective
	- Take the contract average of the bid and ask
	- $\text{Fair Price} = \frac{(\text{Best Bid}\times \text{Best BidQty}) + ({\text{Best Ask}\times \text{Best AskQty}})}{\text{Bid Contracts + Ask Contracts}}$
		- = 383.875
			- $\frac{194561.25 + 197760} {1022}$
