# 🛡️ End-to-End Fraud Detection Pipeline

## 📌 Project Overview
This repository contains the solution for the **Final Term Machine Learning Task 1**. The main objective is to design and implement an end-to-end machine learning and deep learning pipeline to predict the probability of fraudulent online transactions.

Using the **IEEE-CIS Fraud Detection dataset**, this project tackles challenges such as **high-cardinality features** and **extreme class imbalance** (Fraud cases < 3.5%).

## 🎯 Repository Purpose
- To demonstrate the implementation of a complete Data Science pipeline: Data Ingestion → Feature Engineering → Modelling → Evaluation.
- To compare the performance of **Gradient Boosting (LightGBM)** vs **Deep Neural Networks (DNN)** on tabular data.
- To implement strategies for handling imbalanced datasets (Class Weighting & Sampling).

## 🧠 Models & Methodology

### 1. Data Preprocessing & Engineering
- **Memory Reduction:** Optimized data types to reduce memory usage by ~70%.
- **Feature Engineering:** - Extracted time-based features (`hour`, `day`) from `TransactionDT`.
  - Created **Frequency Encoding** for high-cardinality categorical features (e.g., card IDs, addresses).
- **Handling Imbalance:** Applied `is_unbalance=True` (LightGBM) and `class_weights` (Neural Network).

### 2. Models Implemented
| Model | Type | Description |
| :--- | :--- | :--- |
| **LightGBM** | Machine Learning | A gradient boosting framework that uses tree-based learning algorithms. Optimized for speed and efficiency. |
| **Deep Neural Network** | Deep Learning | A Multi-Layer Perceptron (MLP) with BatchNormalization and Dropout layers to prevent overfitting. |

### 📊 Results (ROC-AUC Score)
| Model | Validation AUC Score | Conclusion |
| :--- | :--- | :--- |
| **LightGBM** | **0.9602** | *Best Performance* |
| Deep Learning | 0.9246 | Good Baseline |

*(Note: LightGBM generally outperforms standard DNNs on tabular data due to its ability to handle discrete features effectively).*

## yw File Navigation
The code is structured into a single comprehensive notebook:
- **`Finalterm_transaction_data.ipynb`**: Contains the full pipeline:
  - **Phase 1:** Setup & Utility Functions.
  - **Phase 2:** Data Ingestion & Advanced Feature Engineering.
  - **Phase 3:** LightGBM Model Training (Benchmark).
  - **Phase 4:** Deep Learning Model Training (Challenger).
  - **Phase 5:** Evaluation & Submission Generation.

## 👤 Author Identification
* **Name:** Fattah Ahmad Rasyad
* **Class:** TK-46-03
* **NIM:** 1103220215

---
*Built with using Python, LightGBM, and TensorFlow.*
