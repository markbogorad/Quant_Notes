up:: [[Deep Learning MOC]]
tags:: #Machine_Learning 
# Transformers
- The transformer is referred to anything that uses [[Self-Attention]]
- Introduced in "attention is all you need" 2017
- Powerful way of dealing with sequences by **stacking transformer blocks**
	- The deeper the stack the stronger the transformer 
	- Replaced the [[Recurrent Neural Network (RNN)]] approach for sequential learning
		- [[Transformer vs RNN]]
- Basis of LLMs and [[Artificial Intelligence]]
- Styles
	- [[Encoders]] only (left side)
	- [[Decoders]] only (right side)
	- [[Encoder-Decoder Network]]
## Encoder/Decoder Architecture (Specific Style)
![[Pasted image 20250415194320.png]]
- When paired, the decoder can use cross attention to attend to the output of the encoder (layer in between is [[Cross Attention]]) layer
- Input to [[Feedforward Network (FFNN)]] goes to the FNN and also goes into Add and Norm
	- Add and Norm takes result of processing FNN and input to FNN and combines them
	- Skipping is skip connection (residual network)
		- This was not possible in sequential [[Recurrent Neural Network (RNN)]] architecture (pro of the functional architecture)
- All the lines of data flow are vectors (length d)
- Output of the final layer is vector of length D
- Goal of the decoder is to produce a token (one hot encoded vector) of length V that describes the token
	- Decoder translates vector of length d into a one hot encoded
		- Similar to logistic regression -> classifying vector into magnitude of one of the possible tokens
## Weight derivation in transformer
- 1.4 billion weights in ChatGPT 3 architecture