up:: [[Derivatives MOC]]
tags:: #Finance 
# Theta
$$ \Theta = \frac{\partial V}{\partial t}$$
- **The sensitivity of option price to time**
- Measures how much value the option loses daily due to time decay
	- Theta is always a negative number, since options all decay
- Theta is the same for [[Call Option]] and [[Put Option]]
- If you are long the option: you are *paying theta*
- If you are short the option, you are *collecting theta*
## Theta's Relationship to [[Gamma]]
- $\text{"Fair Theta"} = \frac{ 0.5 \times \text{Cash Gamma} \cdot (\text{s.d. \% move})^2} {100} = \frac{\text{Cash Gamma} \cdot (\text{s.d. \% move})^2}{200}$
- Used to see how "Gamma efficient" a portfolio is
	- Find the "fair price" of owning the option, which can help you understand how quickly the option will be sub-optimal as time goes on
## Theta Relationships
![[Pasted image 20240629153930.png]]
- Theta is highest for ATM options near expiration
- 