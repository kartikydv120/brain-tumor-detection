# 🧠 Brain Tumor Detection using CNN (ResNet18)

Classifies brain MRI scans into 4 categories using Transfer Learning with ResNet18 (PyTorch).

---

## 📌 Problem Statement

Brain tumor detection from MRI scans is a critical medical imaging task. Manual diagnosis is time-consuming and prone to error. This project automates the classification of MRI scans into 4 tumor types using deep learning.

---

## 📂 Dataset

- **Source:** [Brain Tumor MRI Dataset – Kaggle](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)
- **Total Images:** 7,000+ MRI scans
- **Classes:** Glioma, Meningioma, No Tumor, Pituitary

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Deep Learning | PyTorch, Torchvision |
| Model | ResNet18 (Transfer Learning) |
| Data Handling | PIL, NumPy |
| Evaluation | Scikit-learn |
| Visualization | Matplotlib |
| Environment | Google Colab |

---

## ⚙️ How It Works

1. Dataset is downloaded directly from Kaggle using `kagglehub`
2. Images are resized to 128×128 and augmented (flip, rotation)
3. ResNet18 is loaded with pretrained ImageNet weights
4. All layers are frozen — only the final classification layer is trained
5. Model is trained for 5 epochs on T4 GPU

---

## 📊 Results

| Class | Precision | Recall | F1-Score |
|---|---|---|---|
| Glioma | 0.86 | 0.83 | 0.85 |
| Meningioma | 0.77 | 0.67 | 0.71 |
| No Tumor | 0.92 | 0.97 | 0.94 |
| Pituitary | 0.84 | 0.93 | 0.88 |
| **Overall Accuracy** | | | **85%** |

---

## 🚀 How to Run

1. Open `brain_tumor_detection.ipynb` in [Google Colab](https://colab.research.google.com/)
2. Go to **Runtime → Change Runtime Type → T4 GPU**
3. Run all cells — dataset downloads automatically via `kagglehub`
4. Training completes in **5–8 minutes**

---

## 📁 Project Structure

```
brain-tumor-detection/
│
├── brain_tumor_detection.ipynb    # Main notebook (training + evaluation)
├── README.md                      # Project documentation
└── brain_tumor_model.pth          # Saved model weights (after running)
```

---

## 🔗 References

- [ResNet Paper – Deep Residual Learning](https://arxiv.org/abs/1512.03385)
- [Kaggle Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)
