up:: [[Deep Learning MOC]]
tags:: #Machine_Learning 
# RNN
- A chain of [[Multilayer Perceptron (MLP)]] networks where the hidden state of each last one carries over
	- Chain of MLPs where the hidden state auto regressively inputs into the next MLP?
-  Has memory of previous running sum (latent state H) -> summary of prefix of the input
	- Take previous running sum, add new input, update new result, repeat
![[Pasted image 20250417195907.png]]
- The meta pre [[Transformers]]
	- [[Transformer vs RNN]]
- Used for sequential tasks 
	- [[Predict the Next Task]]
- Key addition form [[Multilayer Perceptron (MLP)]]
	- There is a loop that allows information to persist across hidden layers
	- Uses a "hidden state" $h_t$ which is basically a summary of everything that has happened
```
x₁ → [RNN Cell] → h₁ → y₁  
x₂ → [RNN Cell] → h₂ → y₂  
x₃ → [RNN Cell] → h₃ → y₃ 
```
### Hidden state update:
$$h_t=σ(W_{xh}{x_t}+W_{hh}h_{t−1}+b_h)$$

Where:
- ht−1​: previous hidden state
- xt​: current input
- Wxh​: input-to-hidden weights
- Whh​: hidden-to-hidden weights (shared across time)
- bh​: bias
- σ: activation function (typically tanh or ReLU)
- Trained with [[Backpropogation Through Time (BPTT)]]
## Problems
- [[Vanishing Gradient Problem]]
- 