oup:: [[Home]]
tags:: #MOC
# Natural Language Processing (NLP)
## Data Collection
- [[Web Scraping]]
## Preprocessing
- [[Preprocessing Text]]
- [[Tokenization]]
- [[Text Normalization]]
	- [[Case Folding]]
	- [[Lemmatization]]
	- [[Morphology]]
	- [[Stemming]]
		- [[Porters Algorithm]]
- [[Handling Rare Words]]
- [[Text Representation]]
	- [[One Hot Encoding]]
	- [[TF-IDF]]
## Feature Engineering
- N-grams (bigrams, trigrams)
- Part-of-Speech (POS) tagging
- Named Entity Recognition (NER)
- Dependency parsing
- Sentiment scores
- Feature Extraction
## Model Selection (Classification)
- [[Naive Bayes]]
- [[MaxEnt Classifier]]
- [[SVM]]
- [[Neural Network]]
- **Sentence segmentation**: Break text into sentences.
- Case Folding
- **Tokenization**: Split sentences into individual words (tokens).
- **Parts-of-speech tagging**: Classify tokens (e.g., nouns, verbs).
- Bigrams
- **Lemmatization**: Standardize word forms (e.g., "running" → "run").
- **Stopword removal**: Exclude common, non-informative words.
- **Dependency parsing** and **named entity recognition**: Analyze sentence structure and extract key entities (e.g., company names).
- Vectorization
- Similarity Metrics:
	- **Jaccard Similarity**: Measures overlap in sentiment terms between filings to identify consistency in tone.
	- **TF-IDF (Term Frequency-Inverse Document Frequency)**: Highlights terms that are rare but important within filings.
	- **Cosine Similarity**: Analyzes the similarity of sentiment vectors across filings over time.
- Dictionary Limitations
	- **Limitations of General Dictionaries**:
	- General-purpose dictionaries misclassify many words in financial contexts (e.g., "liability," "tax").
	- Nearly 74% of words classified as "negative" by the Harvard dictionary are contextually neutral in finance, adding noise to sentiment analysis.
	- The authors create several word lists tailored for financial text, including:
	- **Negative Words** (e.g., "litigation," "misstatement")
	- **Positive Words**
	- **Uncertainty Words**
	- **Litigious Words**
	- **Strong/Weak Modal Words**
- **Methodology Enhancements**:
	- The authors employ term weighting schemes (e.g., **TF-IDF**) to reduce the noise caused by frequent but irrelevant words.
	- The analysis includes regression models with control variables like firm size, book-to-market ratio, and institutional ownership.
- Tokenization
- BERT
- Bag of Words
- Doc2Vec
- **N-grams**: Basic text sequences.
- **Meta-features**: Hand-crafted features (e.g., counts of hashtags, emoticons, part-of-speech tagging).
- **Word Embeddings**: Dense vector representations learned through deep learning (e.g., Word2Vec, GloVe).
- **Best Performing Features**:
    - Meta-features and word embeddings outperform n-grams in isolation.
    - Lexicon-based meta-features (e.g., sentiment lexicons) significantly boost accuracy.
- **Combination Benefits**:
    - Combining meta-features and word embeddings leads to better performance than using either alone.
    - Ensemble learning further improves performance, with sufficient classifier diversity being crucial.
- **Machine Learning Approaches**:
    - Support Vector Machines (SVM) are effective for n-grams, while Random Forests work well for meta-features.
## Training and Fine Tuning
- 
- Sentence Segmentation
	- Done with decision trees
- Viterbi Algorithm
- Maximum Matching (Greedy Algorithm)
	- Works for Chinese
- Naive Bayes
- MaxEnt Classifiers
- N-Gram Modeling
- Statistical Parsing
- Inverted Index
- Tf-idf
- Bayesian NLP - used by hedge funds for trading
	- Turning textual data into numbers 
- [[One Hot Encoding]]
- Label Encoding --> keeps single column structure and gives a unique number to each category instead of giving a unique column to each category with one hot encoding
## Model Evaluation
## Sentiment Analysis
- Ordering Importance
	- Ex: when a sentence says a ton of good things, BUT, the conclusion is that its not that good - more weight in the end
- Negation - more negation in negative senitment
- Connotations of Words
- Clustering Polarity Lexicon
- Turney Algorithm
- Finding Aspect of Sentance
- 







