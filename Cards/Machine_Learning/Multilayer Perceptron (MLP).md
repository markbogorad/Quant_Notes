up:: [[Deep Learning MOC]]
tags:: #Machine_Learning 
# MLP Layers
- MLP is the original [[Neural Network]] structure of 1 input layer, 1 (at least) hidden layer, 1 output layer
- Power comes from nonlinear [[Activation Functions]]
- Multilayer refers to hidden layers
## General Architecture
Forward pass:
1) Pass inputs to input layer
2) Go into hidden layer
	1) preform the mini regression thing $(z_j^{(1)}​=∑​w_{ji}^{(1)}x_i​+b_j^{(1)})$
		- $w_{ji}^{(1)}$ weight from input xi​ to neuron j in hidden layer 1
		- $b_j^{(1)}$: bias term for neuron j
	2) Apply [[Activation Functions]]
		- $a_j^{(1)}​=σ(z_j^{(1)​})$
		- This basically filters the reaction of a [[Neurons]] in the hidden layer thats accustomed to the task
	- It is unknown what each hidden layer actually does
		- Each hidden layer basically answers this: *"What transformation should I apply to my input to help the next layer do better?"*
3) repeat across deeper layers
	- One layer will learn edges of image, another might combine edges into shapes, another might recognize objects
4) Output layer
5) Compare output with a loss function
[[Backpropogation]]
6) Use an optimizer to adjust weights