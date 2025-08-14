# 🚀 COMSYS_WIZARDS

## 👥 Team Details

- **Team Name:** WIZARDS  
- **Team Members:** Baiduryya Garai, Ayush Saha, Antara Pal  
- **Email & Contact:** *baiduryyag@hmail.com*

---

## 🧩 Problem Overview

This project addresses **face analysis under degraded visual conditions** like blur, fog, rain, low light, and overexposure.  
It is divided into two main tasks:

- **Task A: Gender Classification (Binary)**
- **Task B: Face Recognition (Multi-Class)**

---

## 🛠️ Approach and Methodology

### 🔄 Preprocessing

- **Task A**: Images resized to `224×224` and preprocessed using `EfficientNetV2B2` built-in normalization.
- **Task B**: Applied image-specific min-max normalization to scale pixel values to [0, 1].

### 🧠 Model Architectures

- **Task A**:  
  - Used `EfficientNetV2B2` + `LSTM (64 units)`  
  - Classification using `Dense + Softmax`

- **Task B**:  
  - Built a `Siamese Network` using `ResNet50` as shared sub-networks  
  - Identity verification via absolute embedding differences + Dense layer with sigmoid

### ⚙️ Training Strategy

- **Task A**:
  - Optimizer: `Adam`, LR = `0.01`
  - Loss: `Categorical Cross-Entropy`
  - Epochs: `60`, Early stopping with validation loss

- **Task B**:
  - Data: `52,620` image pairs (similar & dissimilar)
  - Loss: `Binary Cross-Entropy`, Optimizer: `Adam`
  - Batch size: `10`, Epochs: `100` batches with shuffling

---

## 💡 Innovation and Highlights

### Task A – Gender Classification
- Combined `EfficientNetV2B3 + LSTM`
- No oversampling – handled imbalance via design
- Full model fine-tuning

### Task B – Face Recognition
- Verification-based identity prediction
- Balanced pair sampling strategy
- Lightweight absolute embedding difference for comparison

---

## 📈 Results

### Task A: Gender Classification

| Dataset    | Accuracy | Precision | Recall | F1-Score |
|------------|----------|-----------|--------|----------|
| Train      | 100%     | 100%      | 100%   | 100%     |
| Validation | **93.6%**| 94%       | 94%    | 94%      |

- **Male Accuracy:** 86.1%
- **Female Accuracy:** 95.3%

---

### Task B: Face Recognition

| Dataset    | Accuracy | Precision | Recall | F1-Score |
|------------|----------|-----------|--------|----------|
| Train      | 99.55%   | 99.55%    | 99.55% | 99.55%   |
| Validation | **92.17%**| 92.17%   | 92.17% | 92.17%   |
- **Top-1 Accuracy:** **97.66%**
- **macro average f1-score is 92.17%**

---

## 📥 Model Downloads

### 🧠 Task A Model  
📦 **EfficientNetV2B2 + LSTM**  
👉 [Click here to access the Task A Model on Google Drive](https://drive.google.com/file/d/1v-S1mMl5AcPCZBecUQYj_CxX8gl0Ig5x/view)

> ⚠️ Note: Ensure Google sign-in access.

---

### 🧠 Task B Model  
📦 **Siamese Network with ResNet50**  
👉 [Click here to access the Task B Model on Google Drive](https://drive.google.com/file/d/1FRioocZaZHXanVLQfJdGLzP__lYc9E00/view?usp=sharing)

> ⚠️ Note: Ensure Google sign-in access.

---

## 🔮 Conclusion and Future Work

We developed robust and scalable models for face-based gender classification and recognition under visually adverse conditions.  
Future work will explore:
- Augmentation & Restoration methods  
- Enhanced metric learning (e.g., Triplet Loss)  
- Domain-adaptive feature learning

---

## 📎 Submission

📁 **GitHub Repository:** [This Repo](https://github.com/Ayushsaha004/COSMYS_WIZARDS)

---

