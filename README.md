

# UDEx: Universal Adversarial Detection through Explainability

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**UDEx** is a lightweight, model-agnostic framework that leverages *low-rank approximation* and *explainability* (via Grad-CAM) to detect adversarial examples. It is designed to be training-free and scalable across diverse datasets and architectures—including CNNs and Vision Transformers—making it ideal for real-world deployment, especially on resource-constrained devices.

<p align="center">
  <img src="fig1.png" width="600">
</p>

## 🔍 Key Features

- **Explainability-driven**: Uses Grad-CAM to understand model attention.
- **Low-rank reconstruction**: Applies Singular Value Thresholding (SVT) to suppress adversarial perturbations.
- **Training-free**: No need for model retraining or access to labeled adversarial data.
- **Attack & model agnostic**: Works across architectures (CNNs, ViTs) and attack types (FGSM, PGD, CW, etc.).
- **Lightweight**: Suitable for deployment on mobile and edge devices.

---

## 📜 Paper

> **Seeing Through Threats: (UDEx) Universal Adversarial Detection through Explainability**  
> Syamantak Sarkar, Nirmal Joseph, Sudhish N George, Ameer P M, Kiran Raja  
> *Under Review / EUSIPCO 2025 Accepted*  
>  
> 📄 [Paper Link (coming soon)](https://arxiv.org/abs/XXXX.XXXXX)  
> 📁 [Dataset & Models (Google Drive Link)](https://drive.google.com/...)  
> 🔗 [Project Website](https://syamantak-sarkar.github.io/UDEx-Adversarial-Detection/) *(optional)*

---

## 🧠 Method Overview

UDEx detects adversarial attacks by comparing attention maps (Grad-CAM) of original and low-rank approximated images using **Rank-Biased Overlap (RBO)**. A divergence in attention indicates adversarial manipulation.

<p align="center">
  <img src="UDEx_process.png" width="800">
</p>

---

## 📦 Installation

### Requirements
- Python 3.8+
- PyTorch (1.10+)
- OpenCV
- scikit-learn
- matplotlib
- numpy
- tqdm
- scikit-image

### Setup
```bash
git clone https://github.com/syamantak-sarkar/UDEx-Adversarial-Detection.git
cd UDEx-Adversarial-Detection
pip install -r requirements.txt
