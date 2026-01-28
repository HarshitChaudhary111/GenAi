# 🧠 GenAI-Based Chest X-ray Disease Classification  
### DenseNet121 vs Custom CNN (Comparative Study)

---

## 📌 Project Overview
This project presents a **Generative AI–assisted medical imaging system** for automated chest X-ray disease classification. The primary objective is to **compare a pretrained DenseNet121 model with a custom-built CNN model** developed from scratch.

The system also integrates **Explainable AI (XAI)** using **Grad-CAM** to visualize critical lung regions influencing model predictions.

---

## 🎯 Objectives
- Classify chest X-ray images into multiple disease categories  
- Compare transfer learning and custom CNN performance  
- Evaluate accuracy and generalization capability  
- Apply Grad-CAM for model interpretability  

---

## 🗂️ Dataset
- **Type:** Labeled Chest X-ray Images  
- **Classes:**
  - COVID-19  
  - NORMAL  
  - PNEUMONIA  
  - TUBERCULOSIS  

### 🔹 Preprocessing
- Image resizing to `224 × 224`  
- Normalization  
- Data augmentation techniques  

---

## 🏗️ Models Implemented

### 🔹 DenseNet121 (Transfer Learning)
- Pretrained on ImageNet  
- Fine-tuned for 4-class classification  
- Efficient feature reuse and deep connectivity  

**Accuracy:** **87.68%**

---

### 🔹 Custom CNN (Proposed Model)
- Designed and trained from scratch  
- Multiple convolution, pooling, and dense layers  
- Optimized for chest X-ray classification  

**Accuracy:** **80.54%**

---

## 📊 Model Performance Comparison

| Model        | Accuracy (%) |
|-------------|--------------|
| DenseNet121 | **87.68**    |
| Custom CNN  | 80.54        |

### 🔍 Key Observations
- DenseNet121 achieved higher accuracy due to transfer learning  
- Custom CNN performed competitively despite limited training data  
- Transfer learning improves feature extraction and generalization  

---

## 📌 Conclusion
The results show that **DenseNet121 outperforms the custom CNN** due to pretrained knowledge and superior feature extraction. However, the custom CNN demonstrates strong potential and can be further improved with architectural tuning and larger datasets.

Explainable AI techniques like **Grad-CAM** enhance model reliability, making the system suitable for healthcare-related applications.


## 📎 Acknowledgements
This project was developed as part of a **GenAI academic project** for comparative analysis of deep learning models in medical imaging.

<img width="1865" height="852" alt="Screenshot 2026-01-29 033134" src="https://github.com/user-attachments/assets/0f136e8d-e085-4d96-bd7d-3ecc6f712c27" />

