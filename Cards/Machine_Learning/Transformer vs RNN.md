up:: [[Deep Learning MOC]]
tags:: #Machine_Learning 
# [[Transformers]] vs [[Transformer vs RNN]]
- Direct function approach is better for dealing with sequences (replaced looping)
	- Process all inputs in parallel vs sequentially -> gain parallelism
		- Able to deal with rly long sequences and no more vanishing gradient problem
- Loses power of ordering that was in RNN

|Feature|**RNN**|**Transformer**|
|---|---|---|
|🔁 **Structure**|Processes one step at a time (sequentially)|Processes **entire sequence in parallel**|
|🔗 **Dependency modeling**|Learns through recurrence and hidden state|Learns via **attention** over all positions|
|🧠 **Memory**|Encoded in hidden state passed across time|Modeled via **self-attention weights**|
|⏱️ **Speed**|Slow (can’t parallelize over time)|Fast (fully parallelizable)|
|🏗️ **Input flow**|xt,ht−1→htxt​,ht−1​→ht​|All xixi​ → **attention** → all outputs at once|
|🔍 **Interpretability**|Hard to inspect internal memory|Attention weights are inspectable|
|📦 **Core operation**|Autoregressive hidden state update|**Attention over all tokens + feedforward**|