up:: [[Deep Learning MOC]]
tags:: #Machine_Learning 
# Embeddings
- Learnable lookup table
- Embeddings are solution to not being able to one hot encode in NLP
- Intuition
	- When you multiply a one-hot vector by an embedding matrix you get the corresponding row from the table
		- This reduces computation time by allowing for direct indexing 
		- More momoery efficient (embeddings are smaller than one-hot vectors)
## Word2Vec
- An embedding method
- Components:
- ![[Pasted image 20250417193153.png]]
	- Skip-gram
		- The input is used to predict surrounding inputs within a certain band
			- Retrieves the embedding of the input word via an embedding matrix
			- Then it goes into a 1 layer [[Neural Network]]
			- Then [[Softmax]] is applied which assigns likelihood of each word appearing in context
			- Loss: softmax is compared to one hot encoded comparable and minimized with [[Cross Entropy Loss]]
		- More accurate than CBOW
	- Continuous Bag of Words (CBOW)
		- Takes embeddings of surrounding words, sums them, and maps to an output
		- Quicker than CBOW