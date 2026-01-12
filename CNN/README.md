# 🐟 End-to-End Image Classification Pipeline (Fish Dataset)

## 📌 Project Overview
This repository contains the solution for the **Final Term Machine Learning Task 3**. The objective is to build a high-performance Image Classification pipeline to classify **31 different species of fish**.

The project implements Convolutional Neural Networks (CNN) from scratch and compares it with state-of-the-art Transfer Learning methods.

## 🎯 Repository Purpose
- To demonstrate the complete Computer Vision pipeline: Image Loading → Augmentation → Training → Inference.
- To solve **Class Imbalance** issues using computed Class Weights.
- To compare a custom CNN architecture against a pre-trained **MobileNetV2**.

## 🧠 Models & Methodology

### 1. Data Pipeline
- **Optimization:** Utilized `tf.data.AUTOTUNE`, `cache()`, and `prefetch()` for high-speed training.
- **Augmentation:** Applied Random Rotation and Flip to improve model generalization.
- **Handling Imbalance:** Calculated weights for each of the 31 classes to prevent bias towards majority classes.

### 2. Models Implemented
| Model | Type | Architecture |
| :--- | :--- | :--- |
| **CNN From Scratch** | Custom | 3 Convolutional Blocks + GlobalAveragePooling + Dropout. |
| **MobileNetV2** | Transfer Learning | Pre-trained on ImageNet, frozen base layers + custom classification head. |

### 📊 Results
| Model | Accuracy | Training Time |
| :--- | :--- | :--- |
| CNN Scratch | ~60-70% | Slow |
| **MobileNetV2** | **>90%** | **Fast & Efficient** |

*MobileNetV2 significantly outperforms the custom model due to its pre-learned feature extractors.*

## 📂 File Navigation
- **`Finalterm_CNN_vfast.ipynb`**: The optimized notebook containing:
  - **Setup:** Fast local data pipeline configuration.
  - **Training:** Comparison between Scratch CNN and MobileNetV2.
  - **Evaluation:** Confusion Matrix and Classification Report (Precision/Recall/F1).
  - **Inference:** A dedicated section to upload and predict custom fish images.

## 👤 Author Identification
* **Name:** Fattah Ahmad Rasyad
* **Class:** TK-46-03
* **NIM:** 1103220215

---
*Built with using TensorFlow, Keras, and MobileNetV2.*