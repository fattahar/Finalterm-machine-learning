# 🎵 Song Release Year Prediction (Regression Pipeline)

## 📌 Project Overview
This repository contains the solution for the **Final Term Machine Learning Task 2**. The goal is to build an end-to-end regression pipeline to predict the **release year of a song** based on its audio characteristics (timbre features).

The dataset is a subset of the **Million Song Dataset**, containing 90 continuous audio features per song.

## 🎯 Repository Purpose
- To solve a regression problem using both traditional Machine Learning and Deep Learning approaches.
- To demonstrate effective data scaling techniques (`StandardScaler`) crucial for audio data.
- To visualize model performance using Learning Curves and Actual vs. Predicted plots.

## 🧠 Models & Methodology

### 1. Preprocessing
- **Data Cleaning:** Handling missing values (if any) and renaming headerless columns.
- **Scaling:** Applied `StandardScaler` to normalize the 90 timbre features, ensuring stability for the Neural Network.

### 2. Models Implemented
| Model | Type | Description |
| :--- | :--- | :--- |
| **XGBoost Regressor** | Machine Learning | Uses Histogram-based gradient boosting for fast training on large datasets (500k+ rows). |
| **Deep Neural Network** | Deep Learning | A deep architecture (3 Hidden Layers) with `ReLU` activation and a linear output layer. |

### 📊 Results (Root Mean Squared Error)
The primary metric used is **RMSE** (lower is better), representing the average error in years.

| Model | RMSE Score | MAE Score |
| :--- | :--- | :--- |
| **XGBoost** | **9.xxx** | *Best Performance* |
| Deep Learning | 9.xxx | Competitive Performance |

## 📂 File Navigation
- **`Finalterm_Regresi.ipnyb`**: The main notebook containing:
  - Data loading from Google Drive.
  - Standardization of audio features.
  - XGBoost training with `eval_set` logging.
  - Keras Neural Network training with Learning Curve visualization.
  - Final comparative analysis (Bar Charts & Scatter Plots).

## 👤 Author Identification
* **Name:** Fattah Ahmad Rasyad
* **Class:** TK-46-03
* **NIM:** 1103220215

---
*Built with ❤️ using Python, XGBoost, and Keras.*
