up:: [[Deep Learning MOC]]
tags:: #Machine_Learning 
# Functional Style Coding
- Functional vs sequential modeling
```
import tensorflow as tf

inputs = tf.keras.Input(shape=(3,))
x = tf.keras.layers.Dense(4, activation=tf.nn.relu)(inputs) # dense layer 1 (hidden layer) where inputs is passed as an argument (this is how they connect)
outputs = tf.keras.layers.Dense(5, activation=tf.nn.softmax)(x) # dense layer 2 (classifier)
model = tf.keras.Model(inputs=inputs, outputs=outputs) # this maps the inputs and outputs layers (ex if outputs = x it would be mapped to hidden layer)
```
- Uses functions with multiple input layers and multiple output layers (wasn't a thing in sequential)
	- Title of request, body of request
## Layer Objects
- Takes an input -> does a transformation -> get output
	- Encoder is a layer
- Model does the same
	- Difference: model also responds to fit method (gradient descent bit)
	- Model method is where transformer is
- Neural networks will consist of both models and layers as components
## Call Function
- This is what actually runs the network through the model
- Defines the data flow of the model
## Init
- [[__init__]] defines components
## Defining in Call Method vs Init
- Layers are meant to be instantiated in init not call
## Priority
- Binary [[Cross Entropy Loss]] function
- Setting one factor as more important than another than output (ex: 5 times more important to get X than Y)
## Train step
- Can overwrite and make a custom in [[Keras]]
	- A sub component of `fit`
- Can be used to graph intermediate steps of neural net
- Ex: [[Variational Auto-Encoder]]
- Training is done with the "predict the next" method in NLP
- Choosing right learning rate is hard
	- Use custom learning rate schedule
		- Creates a function that computes learnrng rate as a function of epoch number