up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning 
# Unit Length Scaling
$$x_{\text{scaled}} = \frac{x}{\|x\|}$$
Where the norm $( \|x\| )$ is typically the Euclidean norm $(( L^2 )$-norm), defined as:
- $\|x\| = \sqrt{\sum_{i=1}^n x_i^2}$
- Each component is
	- $x_{\text{scaled}, i} = \frac{x_i}{\|x\|}$
## What it does
- Normalization to unit norm -> we effectively transform the vector so that it's length (magnitude) is 1 but it's direction is the same