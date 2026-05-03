# 🛡️ Semantic Shield: Vector-Based LLM Guardrail

> A lightweight, highly efficient K-Nearest Neighbors (KNN) anomaly detection layer operating entirely in the embedding space to intercept LLM prompt injections and roleplay jailbreaks.

**Author:** Waleed Saeed (21i-1672)  
**Affiliation:** *Department of Computer Science, FAST National University of Computer and Emerging Sciences (FAST NUCES), Islamabad*  
**Repository:** [llm-vector-guardrail](https://github.com/WaleedSaeed027/llm-vector-guardrail.git)

---

## 🚀 Overview
As Large Language Models (LLMs) undergo extensive alignment, adversarial actors have developed sophisticated "jailbreak" strategies that reliably bypass standard safety training. **Semantic Shield** shifts the defense paradigm from the generative text domain to the continuous vector domain. 

By projecting inputs into a dense vector space using a frozen sentence-transformer architecture and applying semantic distillation, Semantic Shield acts as a transparent, ultra-fast proxy that intercepts malicious intent before it ever reaches the generative core.

### ✨ Key Performance Metrics
* **Accuracy:** 97% overall accuracy against complex adversarial benchmarks.
* **Security (Recall):** 100% recall rate (Zero False Negatives on malicious payloads).
* **Speed:** 10.03 ms average real-time inference latency (50x-100x faster than LLM-based evaluators like Llama-Guard).

---

## 📂 Repository Structure

This repository contains the complete working code, model assets, and the final research paper detailing the methodology.

* **`Images/`**: Contains performance visualizations, including the confusion matrix and evaluation reports.
* **`Model/`**: Contains the FAISS index, frozen embeddings, and customized vector database clusters.
* **`i211672_NLP_Project_Code.ipynb`**: The main Jupyter Notebook containing the data pipeline, semantic distillation layer, KNN classifier, and evaluation metrics.
* **`researchpaper.pdf`**: The full IEEE-formatted research paper detailing the theoretical framework, architecture, and deep error analysis.

---

## ⚙️ Architecture pipeline
1. **Semantic Distillation:** Strips conversational camouflage (stop words, polite framing) to expose core intent.
2. **Vector Space Mapping:** Converts distilled prompts into dense vectors using the `all-MiniLM-L6-v2` transformer.
3. **FAISS Indexing:** Utilizes a highly optimized Facebook AI Similarity Search flat structure for sub-millisecond neighbor retrieval.
4. **Customizable Thresholding:** Applies a tunable voting threshold (V) to accommodate varying enterprise risk appetites without requiring costly model retraining.

---

## 💻 How to Run

1. Clone the repository:
   
```bash
   git clone [https://github.com/WaleedSaeed027/llm-vector-guardrail.git](https://github.com/WaleedSaeed027/llm-vector-guardrail.git)
   cd llm-vector-guardrail