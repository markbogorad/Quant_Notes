up:: [[Deep Learning MOC]]
tags:: #Machine_Learning 
# Decoder
- The decoder works in an autoregressive manner to produce the output
- Loops 1 token at a time:
	- Input at iteration T = t-1 tokens produced previously + appended token t 
		- Next iteration produces T+1 conditional on previously generated tokens
- Input to the decoder is the previous outputs
### Components
- self attention layer
- cross attention layer
- feed forward network
## In Encoder-Decoder Architecture
- Uses self attention to see which parts of it's inputs are most important to attend to (own input)
	- Uses output of this self attention to query the output of the encoder (referred via cross attention)
		- Query is decided as a result of the first attention layer on its own inputs
	- Think of this as referring back to previous tokens to made a decision (self attention to own input)
- TLDR: The decoder uses inference on it's own inputs to make inferences and queries on the encoder
## Decoder Only Use
- Most AI assistant are decoder only (creates answer 1 token at a time)
- [[Generative Pre-Trained Transformers (GPT)]] is this