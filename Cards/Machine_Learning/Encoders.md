up:: [[Deep Learning MOC]]
tags:: #Machine_Learning 
# Encoders
- Uses self attention to process it's inputs
	- [[Attention]]
	- Can look at all elements simultaneously and chose most important ones to focus on (attend on)
		- RNN had to be sequential, this is done across elements
	- First layer if encoder is self attention to input 
	- Output of attention is routed to an FNN
		- Output of FNN is output of encoder
	- Inside FNN there are 2 [[Dense Layers]]
		- 1st layer takes input vector and expands it to higher dimension (typically 4x input)
		- 2nd layer compresses the expanded dimension and compresses it back
		- Knowledge in the [[Neural Network]] is believed to reside in the FNN layer
			- LLMs work like this - factual knowledge from training data is stored in transformed and it is believed to be stored in FNN
### Components
- Self attention layer
- Feedforward layer
## Encoder Only Use Cases
- Takes 1 vector and translates in into a vector of equal length
- **Sentiment use case (positive/negative) classification**
- Captures meaning within context
- Uses self attention to attend to all of the tokens
- Semantic Search (search engines) (aka [[Embeddings]])
	- Summarization technique
	- Query and run all the documents through an encoder and the encoder will summarize
	- Need documents who's encoding is similar to encoding of a query
	- Vector will capture entire meaning of document