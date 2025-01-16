up:: [[Artificial intelligence MOC]]
tags:: #Machine_Learning 
### How do LLMs work?

1. **Text Data**: Massive corpus of diverse text (e.g., "The quick brown fox jumps over the lazy dog.")
2. **Tokenization**: Breaking text into tokens (e.g., `["The", "quick", "brown", "fox", "jumps", "over", "the", "lazy", "dog", "."]`)
3. **Embedding**: Converting tokens to vectors (e.g., `"fox"` → `[0.2, -0.5, 0.8, ...]`)
4. **Artificial Neural Networks (ANNs)**: Interconnected layers of neurons processing information ([[Neural Network]])
5. **Transformer architecture**: Self-attention based model structure (e.g., BERT, GPT)
6. **Attention mechanism**: Focusing on relevant parts of input (e.g., highlighting "fox" and "jumps" when answering "What did the fox do?")
7. **Next Token Prediction**: The core function of generating text by predicting the most likely next token (e.g., given "The quick brown", predicting "fox")
8. **Context Size**: The number of tokens the model can consider at once (e.g., 2048 or 4096 tokens)
9. **Natural Language Processing (NLP)**: Techniques for language understanding (e.g., parsing sentences, identifying parts of speech) ([[NLP Natural Language Processing MOC]])
10. **Pre-training and fine-tuning**: Initial broad training, then task-specific refinement (e.g., pre-train on books, fine-tune for medical texts)
11. **Contextual understanding**: Maintaining conversation context within the context size (e.g., understanding "it" refers to "the fox" in a follow-up question)
12. **Continuous learning and updates**: Regular model improvements (e.g., adding new words, refining responses based on feedback)