# Cancer Detection with T-cell Infiltration Analysis using CNN

A deep learning project that uses a **Convolutional Neural Network (CNN)** to detect cancer from histopathology images and to analyse **T-cell infiltration** in the tissue.

---

## Table of Contents

1. [Overview](#-overview)
2. [Background](#-background)
3. [Repository Structure](#-repository-structure)
4. [Approach](#-approach)
5. [Getting Started](#-getting-started)
6. [Results](#-results)
7. [Limitations & Future Work](#-limitations--future-work)
8. [Disclaimer](#-disclaimer)


---

## Overview

Manual examination of tissue slides by pathologists is time-consuming and can vary from person to person. This project explores how a CNN can help by:

- **Classifying** tissue images as cancerous / non-cancerous.
- **Studying T-cell infiltration**, i.e. how much the immune system's T-cells have entered the tumour region.

The full workflow (data loading → preprocessing → model training → evaluation) is implemented in a single Jupyter Notebook.

---

## Background

| Term | Simple meaning |
|------|----------------|
| **CNN** | A neural network that learns visual patterns (edges → textures → shapes) directly from images. |
| **Histopathology** | Microscopic study of tissue samples to diagnose disease. |
| **T-cells** | Immune cells that identify and attack abnormal cells, including cancer cells. |
| **T-cell infiltration** | The presence and density of T-cells inside a tumour. It is widely studied as an indicator of immune response and patient prognosis. |

**Analogy:** Think of the tumour as a fort and T-cells as soldiers. Infiltration analysis checks how many soldiers actually managed to get *inside* the fort.

---

## Repository Structure

```
Cancer-with-T-cell-Infiltration-Detection-
│
├── cnn-model-cancer-detection-and-tcell-infiltration.ipynb   # Main notebook (model + analysis)
├── histograms/                                               # Histogram plots generated during analysis
└── README.md                                                 # Project documentation
```

---

## Approach

The pipeline follows the standard CNN workflow:

1. **Data Loading** – Import the image dataset and labels.
2. **Preprocessing** – Resize, normalise and (optionally) augment images.
3. **Exploratory Analysis** – Visualise data distributions using histograms (see `histograms/`).
4. **Model Building** – Design and compile the CNN architecture.
5. **Training** – Train the model on the training split and validate on held-out data.
6. **Evaluation** – Measure performance using metrics such as accuracy and recall.
7. **T-cell Infiltration Analysis** – Interpret the results with respect to T-cell presence in tissue.

<!-- TODO: Update the steps above to match exactly what your notebook does. -->

### Tech Stack

- **Language:** Python 3
- **Environment:** Jupyter Notebook / Kaggle / Google Colab
- **Libraries:** TensorFlow / Keras (or PyTorch), NumPy, Pandas, Matplotlib, Scikit-learn

<!-- TODO: Keep only the libraries actually imported in your notebook. -->

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/AI-ML-Groupnumber-136-2026/Cancer-with-T-cell-Infiltration-Detection-.git
cd Cancer-with-T-cell-Infiltration-Detection-
```

### 2. Install dependencies

```bash
pip install numpy pandas matplotlib scikit-learn tensorflow jupyter
```

### 3. Get the dataset

<!-- TODO: Add dataset name, source link and download instructions here. -->

Download the dataset and place it in the path expected by the notebook (check the data-loading cell).

### 4. Run the notebook

```bash
jupyter notebook cnn-model-cancer-detection-and-tcell-infiltration.ipynb
```

Run all cells from top to bottom. The notebook can also be uploaded to **Kaggle** or **Google Colab** if you want free GPU access.

---

## 📊 Results


Cancer Detection
|Model|	Train Acc.|	Recall|

|------|----------------|
|CNN (Transfer)	|98.03%|	98%|

Til Infiltration Detection
|Model|	Train Acc.|	Positive Recall|
|------|----------------|
|CNN (Transfer)|	74.67%|	77%|
|------|----------------|
|ViT(Transfer)|	69.91%|	79%|



```markdown
(https://github.com/AI-ML-Groupnumber-136-2026/Cancer-with-T-cell-Infiltration-Detection-/tree/main/histograms)
```

---

## Limitations & Future Work

- Evaluate on a larger and more diverse dataset to improve generalisation.
- Try transfer learning with pretrained models (ResNet, EfficientNet, DenseNet).
- Add explainability (e.g. Grad-CAM) to highlight regions that influence predictions.
- Build a simple web interface for uploading an image and getting a prediction.
- Validate results with domain experts (pathologists).

---

## ⚠️ Disclaimer

This project is built **for academic and educational purposes only**. It is **not** a medical device and must not be used for real clinical diagnosis or treatment decisions.


⭐ If you found this project useful, consider giving it a star!
