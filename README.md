# Deepfake Detection using Soft Voting Ensemble

A robust deep learning framework for **binary deepfake image detection** using an ensemble of Convolutional Neural Networks (CNNs) and Vision Transformer (ViT) models. The framework combines the predictions of five state-of-the-art architectures using a **Soft Voting Ensemble** to improve detection accuracy and reliability.

---

## 📌 Project Overview

Deepfake images generated using AI have become increasingly realistic, posing serious threats to digital security and misinformation detection. This project proposes an ensemble-based approach that integrates multiple deep learning models to accurately classify facial images as **Real** or **Fake**.

The proposed framework uses:

- EfficientNet-B0
- ConvNeXt-Tiny
- Vision Transformer (ViT)
- Swin Transformer
- DeiT-Small

Their prediction probabilities are combined using **Soft Voting**, resulting in improved overall performance.

---

## 🏗️ Architecture

<p align="center">
<img width="1536" height="1024" alt="ChatGPT Image Jul 19, 2026, 10_18_46 PM" src="https://github.com/user-attachments/assets/7bc75734-48ac-4bef-9262-dffcf20cc474" />
</p>

---

## 📂 Dataset

**Dataset:** FaceForensics++ (C23)

The dataset contains manipulated and authentic facial images used for training and evaluation.

Dataset preprocessing includes:

- Face Detection
- Face Alignment
- Image Resizing (224 × 224)
- Normalization
- Train / Validation / Test Split

---

## 🚀 Models Used

| Model | Type |
|--------|------|
| EfficientNet-B0 | CNN |
| ConvNeXt-Tiny | CNN |
| Vision Transformer (ViT) | Transformer |
| Swin Transformer | Hierarchical Transformer |
| DeiT-Small | Data-Efficient Vision Transformer |

---

## ⚙️ Ensemble Strategy

The outputs of all five models are combined using **Soft Voting**.

Final Prediction:

```
Final Probability =
(P1 + P2 + P3 + P4 + P5) / 5
```

The class with the highest averaged probability is selected as the final prediction.

---

## 📊 Performance

| Model | Accuracy | Precision | Recall | F1-Score | AUC |
|--------|---------:|----------:|--------:|---------:|----:|
| EfficientNet-B0 | 90.80% | 87.17% | 98.87% | 92.65% | 92.23% |
| ConvNeXt-Tiny | 92.07% | 88.41% | 99.53% | 93.64% | 92.94% |
| Vision Transformer | 91.63% | 99.50% | 80.13% | 88.77% | 91.24% |
| Swin Transformer | **92.29%** | 99.67% | 81.60% | **89.74%** | 92.49% |
| DeiT-Small | 92.12% | 99.19% | 81.60% | 89.54% | 92.39% |
| **Soft Voting Ensemble** | **92.18%** | **99.84%** | **81.20%** | **89.56%** | **91.95%** |

---

## 📈 Results

### Confusion Matrix

<p align="center">
<img src="ensemble_confusion.png" width="450">
</p>

### ROC Curve

<p align="center">
<img src="ensemble_roc.png" width="450">
</p>

---

## 🛠️ Technologies Used

- Python
- PyTorch
- timm
- TorchVision
- NumPy
- Pandas
- OpenCV
- Matplotlib
- Scikit-learn

---

## 📁 Project Structure

```
Deepfake-Detection/
│
├── dataset/
├── models/
│
├── train.py
├── test.py
├── ensemble.py
│
├── figure.png
├── ensemble_confusion.png
├── ensemble_roc.png
│
├── requirements.txt
└── README.md
```

---

## ▶️ Installation

Clone the repository

```bash
git clone https://github.com/your-username/Deepfake-Detection.git
```

Move into the project directory

```bash
cd Deepfake-Detection
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Training

```bash
python train.py
```

---

## ▶️ Testing

```bash
python test.py
```

---

## 📌 Key Features

- Ensemble of five state-of-the-art deep learning models
- Soft Voting based prediction
- High precision (99.84%)
- Robust binary deepfake detection
- FaceForensics++ benchmark dataset
- Easy to extend for multi-class deepfake detection

---

## 🔮 Future Work

- Multi-class deepfake detection
- Video-level temporal modeling
- Multimodal (Audio + Video) learning
- Attention-based fusion strategies
- Evaluation on larger benchmark datasets

---

## 📚 References

1. FaceForensics++: Learning to Detect Manipulated Facial Images (ICCV 2019)
2. EfficientNet: Rethinking Model Scaling for CNNs (ICML 2019)
3. Vision Transformer (ICLR 2021)
4. Swin Transformer (ICCV 2021)
5. DeiT (ICML 2021)
6. ConvNeXt (CVPR 2022)

---

## 👨‍💻 Author

**Priyam Chaudhary**

B.Tech Computer Science and Engineering

Thapar Institute of Engineering and Technology

GitHub: https://github.com/priyam9002

LinkedIn: https://www.linkedin.com/in/priyam-chaudhary-a9477b273/


---

⭐ If you found this project useful, consider giving it a **Star** on GitHub.
