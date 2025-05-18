up:: [[Deep Learning MOC]]
tags:: #Machine_Learning 
# Neural Network
- *Core idea: the neural network is a function approximator that works by learning a ton of input-output pairs to be able to predict outputs from inputs eventually*
- Provide the training samples in batches and they are optimized via [[Gradient Descent]]
- An optimization solution
	- Minimizing discrepancy between predicted and true values
- Can work with non stationary data
## General Overview of how it works
- A sequence of layers
	- Input layer -> hidden layer -> output layer (see [[Layers (Neural Networks)]])
- Layer $l$ transforms its input $y_{l-1}$ into the output $y_l$
	- Layer takes the output of a previous layer and transforms it into something else ([[Transformers]])
- Middle layers transform the input into synthetic features which makes it easier for classifier or regressor to solve the problem
	- Transforming inputs into outputs but not very interoperable what is here
	- Transforming vector lengths to make it work better
	- Theory: middle layers are learning alternate combos at increasing complexity
- Final layer solves a [[Regression]] or [[Classification]] task
	- Classifier output
		- Chooses 1 class from a discrete set of classes
		- Transforms a vector of length Y_{l-1} into a vector of length C 
			- C is a probability distribution over the classes
## Types of Neural Networks
- [[Recurrent Neural Network (RNN)]]
- [[Long Short Term memory (LSTM) Network]]
- [[Feedforward Network (FFNN)]]
- [[Transformers]]