up:: [[Machine Learning Miscellaneous MOC]]
tags:: #Programming 
# Gradient Descent
- Gradient descent is an optimization algorithm used to minimize a function by iteratively moving towards the function's steepest descent, or minimum
![[90062gdopt.gif]]
- Defining a cost function --> find gradient of cost function (error)
	- Iteratively predict until the gradient has reached minimum threshold
	- For loop in [[Python MOC]]
## Popular Gradient Descent Techniques
- Stochastic gradient descent - calculate gradient using a random training example.
    - Memory Cue: "Stochastic" implies "Random," i.e., a single, random example at each step.
- Mini-batch gradient descent - calculate gradient use a sub-sample (=min-batch) of training examples.
    - Memory Cue: "Mini-Batch" implies a "Small Batch" or subset of the training data.
- Batch gradient descent - calculate gradient using entire training sample (=batch)
    -  Memory Cue: Think "Batch" as "Whole Batch" of data.
## Learning rate
- size of each step taken in gradient descent
- Why the steps are important
- ![[Pasted image 20240829180127.png]]