up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# Decision Trees
- ![[Pasted image 20240830071259.png]]
- Each leaf node on the left corresponds to some region in the right, where we visualize such a space.
- We can now easily determine the output value by determining in which region the input point falls for a given input
- Used in option pricing
	- Splits on some sort of threshold
	- stopping the tree

## Formally
$$f(x) = \sum_{m=1}^{M} c_m \mathbb{I} [x \in R_m]$$
- where R_m refers to the respective region for all regions M.
- constant c_m which is what we output for the region R_m​
- We have to identify in which region x belongs.
- The I is an indicator function ([[If-Else Statements]]), that simply means that `if I[statement=true]:= 1, \space else \space0`
## In [[Python MOC]]
```
Given the value x:
for m in M:
	if x in Rm:
		y = 1 * c
	elif x not in Rm:
    y = 0 * c
```