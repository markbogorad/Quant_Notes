up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# Neural Network
> Within finance we can use neural networks for so many things like feature extraction, data generation, classification, regression, ranking, survival analysis, time series forecasting, optimization…

The idea is simple: the model takes inputs x, multiplies them by weights w, and adds them all together. The sum of the product obtained $\sum_{i=1}^{m} x_{i} w_{i}$ is then passed through a non-linear activation function g. The output of the function give the prediction $\hat{y}$.
$$\hat{y}=g\left(\sum_{i=1}^{m} x_{i} w_{i}\right)$$

- A [[Logistic Regression]] is an oversimplified neural network *important*
- Neural net is a sigmoid on top of a sigmoid on top of a sigmoid 
	- Think of these as the direction of the neural net (up = 1 down = 0) and this goes on for the entire network
- Multi perceptron --> predicting multiple outputs


- 