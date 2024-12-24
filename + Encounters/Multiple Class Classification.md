up:: [[Supervised Learning]]
tags:: #Programming 
# Multiple Class Classification
- The way it was originally done
	- Testing binary classification models (ex: are you from Singapore or the other countries)
		- The one with the highest probability is what we used
- Now
	- Output a vector of probabilities of all binary classification models 
	- Loss function changes from log loss to multi class logistic loss --> goal is to minimize soft-max function
- Not fully reliable because it is biased depending on groups used