up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming #Math 
# Penalty Types
- Penalties are intended to make models less complex 
	- Remove features, and minimize coefficients by focusing on the core relationships and ignoring the weak relationships in the model → penalization is one method of regularization (model simplification).
- L1 -> The L1 norm that is calculated as the sum of the **absolute values** of the vector.
	- [[Lasso Regression]]
- L2 -> The L2 norm is calculated as the the sum of the **squared vector** values.
	- [[Ridge Regression]]
- Elastic
	- Mix of L1 and L2