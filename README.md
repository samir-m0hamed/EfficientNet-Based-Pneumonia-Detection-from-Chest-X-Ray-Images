# Pneumonia Detection via EfficientNet

An advanced medical image classification system for automated Pneumonia detection from Chest X-ray scans using EfficientNet with transfer learning and progressive fine-tuning.

---

## 🔍 Overview

This project implements a binary classifier capable of distinguishing between:

- NORMAL
- PNEUMONIA

The pipeline is built using a pretrained **EfficientNet** backbone and optimized through two structured training phases to achieve strong generalization and high AUC performance.

---

## 🧠 Model Configuration

- Backbone: EfficientNet (Pretrained on ImageNet)
- Input Resolution: 224×224
- Global Average Pooling
- Fully Connected Output Layer
- Sigmoid Activation (Binary Classification)

---

## ⚙️ Training Workflow

### Phase 1 — Feature Extraction
- Backbone frozen
- Classifier head trained
- Faster convergence

### Phase 2 — Fine-Tuning
- Top layers unfrozen
- Reduced learning rate
- Improved feature refinement

---

# 📊 Performance Evaluation

---

## 📈 ROC Curve

![ROC Curve](Pneumonia%20Detection%20via%20EfficientNet/ROC.png)

### ROC Metrics

| Metric | Score |
|--------|--------|
| AUC | **0.989** |

The model demonstrates excellent discrimination capability between classes.

---

## 🧾 Confusion Matrix

![Confusion Matrix](Pneumonia%20Detection%20via%20EfficientNet/confusion%20matrix.png)

### Matrix Values

| Actual \ Predicted | NORMAL | PNEUMONIA |
|--------------------|--------|-----------|
| NORMAL             | 73     | 5         |
| PNEUMONIA          | 12     | 217       |

---

## 📌 Evaluation Metrics (Threshold = 0.5)

| Metric | Value |
|--------|--------|
| Accuracy | 0.945 |
| Precision | 0.977 |
| Recall | 0.948 |
| F1 Score | 0.962 |

---

## 📉 Phase 1 — Feature Extraction Results

![Feature Extraction](Pneumonia%20Detection%20via%20EfficientNet/feature%20extraction%20results.png)

### Final Epoch Summary

| Metric | Train | Validation |
|--------|--------|------------|
| Loss | ~0.11 | ~0.18 |
| AUC | ~0.992 | ~0.985 |
| Accuracy | ~0.955 | ~0.92 |

Observations:
- Strong early convergence
- Minor validation fluctuations
- Stable AUC growth

---

## 📉 Phase 2 — Fine-Tuning Results

![Fine Tuning](Pneumonia%20Detection%20via%20EfficientNet/fine%20tuning%20results.png)

### Final Epoch Summary

| Metric | Train | Validation |
|--------|--------|------------|
| Loss | ~0.10 | ~0.13 |
| AUC | ~0.993 | ~0.987 |
| Accuracy | ~0.958 | ~0.94 |

Observations:
- Reduced validation loss
- Improved generalization
- Balanced bias-variance behavior

---

# 📌 Model Interpretation

- AUC close to 0.99 indicates near-separable feature space
- Low False Positive Rate (only 5 normal misclassified)
- Strong recall on Pneumonia cases
- Suitable for clinical decision-support research scenarios

---

# 🛠️ Technology Stack

- Python
- Keras - Tensorflow
- NumPy
- Scikit-Learn
- Matplotlib
- Plotly

---

# 📂 Repository Structure

```
Pneumonia Detection via EfficientNet/
│
├── Pneumonia_Detection_via_EfficientNet.ipynb
│
├── ROC.png
├── confusion matrix.png
├── feature extraction results.png
├── fine tuning results.png
│
└── README.md
```

---

# 👨‍💻 Author

**Samir Mohamed, AI & computer vision Engineer**
