up:: [[Supervised Learning MOC]]
tags:: #Machine_Learning
# KNN 
- to predict a new input x, you statistically find the K closest points in the training data, and average the corresponding outputs. We can write this as an equation a
$$f(x)=\frac{1}{K}\sum_{n\in \mathrm{Neigh}_{K}(x)}{y^{(n)}}{}$$
- K nearest neighbors
	- KNN cant extrapolate --> the largest value will be the maximum value ever seen in the training data
		- Essentially a ceiling --> disadvantage
 - KNN for classification -> becomes mode (modus) instead of average

K-nearest neighbors (KNN) can be used for both **regression** and **classification** tasks.
- **KNN Classification**: In this case, the algorithm assigns a class to a data point based on the majority class among its k nearest neighbors. It’s commonly used for tasks like image recognition or spam detection, where the output is a discrete label.
    
- **KNN Regression**: Here, the algorithm predicts the value of a continuous variable by averaging the values of the k nearest neighbors. It’s used in situations where the goal is to predict a numerical outcome, such as estimating a house price based on nearby houses.

- Sensitive to [[The Curse of Dimensionality]]
- 