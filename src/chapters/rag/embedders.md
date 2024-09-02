
# Embedders in AI

## Overview

Embedders are algorithms or models used to convert data (e.g., text, images, audio) into a fixed-size vector representation, commonly known as embeddings. These embeddings capture the semantic meaning of the data and are essential in various machine learning and natural language processing tasks.

## Types of Embedders

1. **Word Embeddings**
    - Convert words into dense vectors.
    - Examples: Word2Vec, GloVe, FastText.

2. **Sentence Embeddings**
    - Convert sentences or phrases into dense vectors.
    - Examples: Sentence-BERT, Universal Sentence Encoder.

3. **Document Embeddings**
    - Convert entire documents into dense vectors.
    - Examples: Doc2Vec, Transformer-based models.

4. **Image Embeddings**
    - Convert images into dense vectors.
    - Examples: Convolutional Neural Networks (CNNs), ResNet, Inception.

5. **Audio Embeddings**
    - Convert audio signals into dense vectors.
    - Examples: MFCC, Wave2Vec.

## Applications

- **Information Retrieval**: Efficiently retrieve relevant documents or data.
- **Text Classification**: Classify text into predefined categories.
- **Recommendation Systems**: Provide personalized recommendations.
- **Clustering**: Group similar data points together.
- **Semantic Search**: Improve search results by understanding context and meaning.

## Popular Embedding Models

### Word2Vec

```python
from gensim.models import Word2Vec

# Training Word2Vec model
sentences = [["this", "is", "a", "sample", "sentence"], ["word", "embeddings", "are", "useful"]]
model = Word2Vec(sentences, vector_size=100, window=5, min_count=1, workers=4)

# Getting embedding for a word
word_embedding = model.wv['sample']
print(word_embedding)
```

### BERT (Bidirectional Encoder Representations from Transformers)

```python
from transformers import BertTokenizer, BertModel
import torch

# Initialize BERT tokenizer and model
tokenizer = BertTokenizer.from_pretrained('bert-base-uncased')
model = BertModel.from_pretrained('bert-base-uncased')

# Encode a sentence
sentence = "Embedding models are powerful."
inputs = tokenizer(sentence, return_tensors='pt')
outputs = model(**inputs)

# Get the sentence embedding
sentence_embedding = outputs.last_hidden_state.mean(dim=1).squeeze()
print(sentence_embedding)
```

### Sentence-BERT

```python
from sentence_transformers import SentenceTransformer

# Initialize Sentence-BERT model
model = SentenceTransformer('paraphrase-MiniLM-L6-v2')

# Encode a list of sentences
sentences = ["Embedding models are powerful.", "They convert text into vectors."]
sentence_embeddings = model.encode(sentences)

for sentence, embedding in zip(sentences, sentence_embeddings):
    print(f"Sentence: {sentence}\nEmbedding: {embedding}\n")
```

## Evaluation Metrics

- **Cosine Similarity**: Measures the cosine of the angle between two vectors.
- **Euclidean Distance**: Measures the straight-line distance between two vectors.
- **Dot Product**: Measures the product of the magnitudes of two vectors and the cosine of the angle between them.

