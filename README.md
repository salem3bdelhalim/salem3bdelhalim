# 👟 Footwear Classifier with Factorized Inception & Spatial Attention

[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow)](https://www.tensorflow.org/)
[![Keras](https://img.shields.io/badge/Keras-Supported-red?logo=keras)](https://keras.io/)
[![Accuracy](https://img.shields.io/badge/Accuracy-96.8%25-brightgreen)](https://github.com/salemabdelhalim1)

## 📝 Project Overview
This repository features a custom-built Deep Learning architecture specifically designed for high-precision classification of footwear (Boots, Sandals, Shoes). The model stands out by combining **Factorized Inception Modules** for efficient feature extraction and a **Spatial Attention Mechanism** to enhance the model's focus on relevant object parts.

---

## 🚀 Key Technical Features

### 1. Factorized Inception Modules
Instead of traditional $3 \times 3$ or $5 \times 5$ convolutions, this model decomposes them into:
* **$1 \times 3$ and $3 \times 1$ layers**: This drastically reduces the number of parameters and computational cost while increasing the non-linearity of the network, allowing it to learn more complex features.

### 2. Spatial Attention Mechanism
The model doesn't just look at the whole image equally. It uses a **Spatial Attention** block:
* **Process**: It applies both `Global Average Pooling` and `Global Max Pooling` across the channel dimension to identify "where" the most important information is located.
* **Benefit**: It suppresses noise from the background and highlights the footwear's structural features.

### 3. Optimized Architecture
* **Input Shape:** $120 \times 120 \times 3$
* **Regularization:** Includes `BatchNormalization` and `Dropout (0.2)` to ensure stable training and prevent overfitting.
* **Efficient Branches:** Merges features from different scales using 1x1, 3x3 (factorized), and 5x5 (factorized) convolutions.

---

## 📊 Performance Results

### 📈 Training Progress
The model shows excellent convergence. After initial fluctuations, the **Validation Loss** stabilizes closely with the **Training Loss**, indicating a well-generalized model.

| Metric | Result |
| :--- | :--- |
| **Final Validation Accuracy** | **~96.8%** |
| **Classes** | Boot, Sandal, Shoe |

### 🧩 Confusion Matrix Analysis
The confusion matrix reveals high precision across all categories:
* **Boots:** Highest accuracy with minimal misclassification.
* **Sandals & Shoes:** Slight, logical confusion due to similar silhouettes in specific designs.

---

## 🛠 Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/salemabdelhalim1/Inception-Spatial-Attention.git](https://github.com/salemabdelhalim1/Inception-Spatial-Attention.git)
