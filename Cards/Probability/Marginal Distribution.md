up:: [[Probability MOC]]
tags:: #Math
# Marginal Distribution
- Deriving the probability of a single variable form a [[Joint Distributions (Discrete vs Continuous)]]
	- A single distribution derived from a joint distribution
- Can't go from single distributions to joint --> missing key dependencies between variables
- But, joint PDF is the product of marginal PDFs
### Marginal PDF
**Discrete Case**
- $p_X(x) = \sum_{y} p_{X,Y}(x,y)$
- $p_Y(y) = \sum_{x} p_{X,Y}(x,y)$
- Example (Discrete Case):
	- Suppose X and Y represent the outcomes of rolling two six-sided dice, and the joint PMF $pX,Y(x,y)$ gives the probability of rolling x on the first die and y on the second die. To find the marginal distribution of X (i.e., the probability distribution of the first die regardless of the second die's outcome):
			$pX​(x)=y=1∑6​pX,Y​(x,y)$
	- For example, if the dice are fair, $pX,Y(x,y)=\frac{1}{36}$​ for all x,y, so:
			$pX(x)=∑y=\frac{1}{36}=\frac{6}{36}=\frac{1}{6}$
This shows that each outcome on the first die has a probability of 1/6​, regardless of the second die's outcome.

**Continuous Case**
- $f_X(x) = \int_{-\infty}^{\infty} f_{X,Y}(x,y) \, dy$
- $f_Y(y) = \int_{-\infty}^{\infty} f_{X,Y}(x,y) \, dx$
- Suppose X and Y are continuous random variables representing the height and weight of individuals, respectively, with a known joint PDF $fX,Y(x,y)$. To find the marginal distribution of height X (regardless of weight):
		$fX(x) = \int_{\infty}^{\infty} f_{X,Y}(x,y) \, dx \, dy$
This integration "sums out" the weight variable YY, leaving the distribution of height X alone.