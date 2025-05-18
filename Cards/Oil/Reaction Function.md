up:: [[Oil Markets MOC]]
tags:: #Finance 
# The Reaction Function
- A way to size into systematic positions ([[Algorithmic Trading in Oil]]) via volatility targeting
- The reaction function optimizes position size
	- Maps strength of signal to size of bet
	- Uses a [[Normal Distribution]] Z score to identify strength of signal via standard deviations
		- This helps smooth reaction to signal
## Example
$$R(x)=xe^{0.5(1-x^2)}$$
![[Pasted image 20250115120508.png]]
- These can be easily adjusted and parameterized however necessary