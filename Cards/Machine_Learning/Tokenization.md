up:: [[Deep Learning MOC]]
tags:: #Machine_Learning 
# Tokenization
- An algorithm used to break downs sentances into numbers 
## Code
```
# Tokenization

def tokenize_function(examples):
	
	return tokenizer(
		
		examples["sentence"],
		
		padding="max_length",
		
		truncation=True,
		
		max_length=512

)
```
## Parameters
| Parameter                  | What it means                                                                | Why it's needed                                                                                                                 |
| -------------------------- | ---------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| **`padding="max_length"`** | Add filler tokens so that **every input is exactly 512 tokens long**.        | Transformers need **fixed-size** batches. Variable sizes would crash training. Think of this as all bricks need to be same size |
| **`truncation=True`**      | **Cut off** tokens if a sentence is too long (over 512 tokens).              | Prevents inputs from exceeding the model's maximum allowed size.                                                                |
| **`max_length=512`**       | Sets the **maximum length** (after padding or truncation) to **512 tokens**. | 512 is the standard input size limit for BERT/DistilBERT models. Size is set by the model                                       |