# cbow-vs-bert-word-embeddings
A hands-on NLP project implementing CBOW from scratch and comparing it with contextual BERT embeddings to understand how modern language models represent meaning.

📌 Project Highlights

✔ Implemented CBOW (Continuous Bag of Words) from scratch using NumPy
✔ Explicit forward & backward propagation (no deep-learning framework shortcuts)
✔ Trained on Tiny Shakespeare corpus (as per academic specification)
✔ Visualized learned embeddings using PCA
✔ Extracted contextual embeddings from BERT
✔ Demonstrated polysemy handling (static vs contextual meaning)
✔ Clear experimental comparison: CBOW vs BERT

This project shows strong fundamentals in NLP, linear algebra, and model internals, not just library usage.

🎯 Objectives

Learn how static word embeddings are trained using CBOW

Understand gradient-based training of embedding models

Explore contextual embeddings using Transformer models

Experimentally compare classical vs modern NLP approaches

📂 Dataset

Tiny Shakespeare Corpus

Preprocessing:

Lowercasing

Whitespace tokenization

Punctuation removal

Train/Test split: 80 / 20

Why Tiny Shakespeare?
It is small enough to train CBOW from scratch, yet rich enough to learn meaningful word co-occurrences.

🧠 Model Overview
🔹 CBOW (From Scratch)

Input: Average of context word one-hot vectors

Context window: 2 (2 left + 2 right)

Hidden layer: W1 (V × D) → word embeddings

Output layer: W2 (D × V)

Loss: Cross-entropy

Optimization: Gradient Descent

Implemented manually, step by step

🔹 BERT

Model: bert-base-uncased

Extracted embeddings from last hidden layer

Used to demonstrate context-aware representations

📊 Experiments & Results
🔍 CBOW Training

Loss decreases consistently across epochs

Confirms correct forward/backward implementation

Learned embeddings capture basic semantic similarity

🎨 Embedding Visualization

PCA shows clustering of semantically related words

Some noise due to limited corpus size (expected)

🧪 Polysemy Experiment (“bank”)
Model	Observation
CBOW	Same vector regardless of context
BERT	Different vectors for different meanings

✔ Clearly demonstrates static vs contextual embeddings

⚔️ CBOW vs BERT — Quick Comparison
Feature	CBOW	BERT
Embedding Type	Static	Contextual
Polysemy Handling	❌	✅
Training Data	Small corpus	Massive pretraining
Interpretability	High	Medium
Real-world NLP	Limited	State-of-the-art
🛠️ Tech Stack
Python
NumPy
Matplotlib
Scikit-learn
Hugging Face Transformers

PyTorch (for BERT inference only)
