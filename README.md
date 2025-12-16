# 🧠 How Do Machines Understand Words?

## CBOW vs BERT — Static vs Contextual Word Embeddings

---

<p align="center">
  <img src="https://img.shields.io/badge/NLP-Word%20Embeddings-blue" />
  <img src="https://img.shields.io/badge/Model-CBOW%20(from%20scratch)-orange" />
  <img src="https://img.shields.io/badge/Model-BERT-green" />
  <img src="https://img.shields.io/badge/Status-Completed-success" />
</p>

---

## 📌 Project Overview

* This project explores **how machines learn word meaning**
* Implements **CBOW from scratch** (no deep-learning framework shortcuts)
* Compares **static embeddings (CBOW)** with **contextual embeddings (BERT)**
* Strictly follows an academic NLP assignment specification
* Presented as a **clean, reproducible Jupyter notebook**

---

## ⚡ Why This Project Matters (Recruiter Perspective)

* Most NLP projects **only use pretrained embeddings**
* This project:

  * builds embeddings **from first principles**
  * implements **manual forward & backward propagation**
  * validates ideas through **experiments and visualizations**
* Demonstrates:

  * strong NLP fundamentals
  * understanding of model internals
  * ability to explain results clearly

---

## 🧩 Core Question Addressed

* ❓ Does a word always have the same meaning?
* 🧪 Experiment:

  * Compare **CBOW** vs **BERT**
* 📌 Example:

  * *“I deposited money in the bank”*
  * *“They sat near the river bank”*

**Expected behavior**

* CBOW → same embedding
* BERT → different embeddings

---

## 🏗️ What Was Built

### 🔹 CBOW Model (From Scratch)

* Implemented using **NumPy only**
* No PyTorch / TensorFlow for CBOW
* Explicit implementation of:

  * one-hot encoding
  * context vector averaging
  * matrix multiplication
  * softmax activation
  * cross-entropy loss
  * gradient descent updates
* Confirms **conceptual mastery**, not library dependency

---

## 📚 Dataset & Preprocessing

* Dataset:

  * **Tiny Shakespeare Corpus**
* Preprocessing steps:

  * lowercasing
  * whitespace tokenization
  * punctuation removal
* Training setup:

  * ordered 80 / 20 train-test split
  * context window = **2 left + 2 right**

---

## 📉 CBOW Training Behavior

* Trained for multiple epochs
* Observed:

  * consistent decrease in training loss
  * stable convergence behavior
* Confirms:

  * correct forward pass
  * correct backpropagation
  * correct parameter updates

---

## 📊 What CBOW Learns

* Captures **co-occurrence-based semantics**
* Similar words move closer in embedding space
* Limitations:

  * one word → one fixed vector
  * no context awareness
  * cannot handle polysemy

---

## 🎨 Embedding Visualization

* Dimensionality reduction using **PCA**
* Observations:

  * semantically related words form clusters
  * rare or ambiguous words appear noisier
* Visualization makes embeddings:

  * interpretable
  * explainable

---

## 🤖 BERT Contextual Embeddings

* Model used:

  * `bert-base-uncased`
* Extracted:

  * token-level embeddings from last hidden layer
* Key behavior:

  * same word → different vectors in different contexts
* Demonstrates:

  * context-aware representation
  * strength of transformer architectures

---

## ⚔️ CBOW vs BERT — Experimental Comparison

| Feature           | CBOW         | BERT                |
| ----------------- | ------------ | ------------------- |
| Embedding type    | Static       | Contextual          |
| Context awareness | ❌            | ✅                   |
| Polysemy handling | ❌            | ✅                   |
| Training data     | Small corpus | Massive pretraining |
| Real-world NLP    | Limited      | State-of-the-art    |

---

## 📊 Key Experimental Findings

* CBOW:

  * loss decreases over epochs
  * embeddings capture basic similarity
  * fails on multi-meaning words
* BERT:

  * embeddings vary with context
  * successfully separates different word senses
* Conclusion:

  * static embeddings ≠ sufficient for real NLP tasks

---

## ▶️ Run the Project (Google Colab)

* Open the notebook directly in Colab:

```
(https://colab.research.google.com/drive/1vfnWeomQRHlnkY_hM8kYnvetBZPIclUu)
```


## 🧠 Skills Demonstrated

* NLP fundamentals
* Neural network training from scratch
* Vector similarity analysis
* Embedding visualization
* Transformer-based contextual embeddings
* Experimental reasoning & interpretation

---

## 🏁 Final Takeaway

* **CBOW** explains *how* word meaning emerges from co-occurrence
* **BERT** explains *why* context is essential
* This project connects:

  * classical NLP theory
  * modern transformer practice

---

Just tell me.
