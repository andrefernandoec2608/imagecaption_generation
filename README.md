# 🖼️ Image Captioning with Deep Learning

A Deep Learning project focused on automatic image caption generation using the **MS COCO 2017 Captions** dataset.

This project implements a complete multimodal image captioning pipeline, combining **Computer Vision** and **Natural Language Processing**. A custom **Encoder–Decoder architecture with attention** was developed in **PyTorch** and compared against the state-of-the-art **BLIP** pretrained image captioning model.

---

## 🔄 Model Overview

```text
Image
  │
  ▼
ResNet50 Encoder
  │
  ▼
Visual Features
  │
  ▼
Transformer Decoder
  │
  ▼
Attention Mechanism
  │
  ▼
Generated Caption
```

---

## 📌 Project Summary

The goal of this project is to generate natural language descriptions for images by training a deep learning model that learns the relationship between visual features and textual captions.

The project covers:

- Image preprocessing and transformation
- Caption tokenization and vocabulary construction
- Custom Dataset and DataLoader implementation
- Encoder–Decoder model development
- Attention-based caption generation
- BLEU score evaluation
- Comparison with BLIP

---

## 🚀 Technologies

### Core Frameworks

- Python
- PyTorch
- Torchvision
- Hugging Face Transformers

### Data and NLP

- MS COCO Captions 2017
- pycocotools
- NLTK

### Visualization and Utilities

- Matplotlib
- NumPy
- PIL

### Environment

- CUDA GPU
- Kaggle

---

## 📚 Dataset

This project uses the **MS COCO 2017 Captions** dataset, a large-scale image captioning dataset containing images paired with human-written captions.

The dataset is used to train and evaluate the custom image captioning model.

---

## 🏗️ Architecture and Implementation

### Data Pipeline

The project implements a complete multimodal pipeline for processing paired image-caption samples.

#### Image Processing

- Image transformations
- Data augmentation
- Batch loading using custom DataLoaders

#### Text Processing

- Caption tokenization
- Vocabulary generation
- Sequence encoding
- Padding and batching

Custom Dataset and DataLoader classes were implemented to efficiently manage image-caption pairs during training and validation.

---

## 🧠 Model Architecture

The custom model follows an **Encoder–Decoder** architecture.

### Encoder

A **ResNet50 CNN** extracts high-level visual features from each image.

### Decoder

A **Transformer Decoder** generates captions one token at a time using the encoded visual representation.

### Attention Mechanism

The attention mechanism allows the decoder to focus on the most relevant visual features while generating each word in the caption.

Additional components include:

- Word embeddings
- Positional encoding
- Configurable caption length generation

---

## ⚙️ Training Strategy

The training pipeline includes techniques designed to improve convergence and generalization:

- Training and validation loops
- Model checkpointing
- Early stopping
- GPU acceleration with CUDA
- Best model restoration

The model was trained on the complete **MS COCO 2017 training split** for **9 epochs**.

---

## 📊 Evaluation

The custom model was evaluated using BLEU scores and compared against the pretrained BLIP image captioning model.

| Metric | Custom Model | BLIP |
|---|---:|---:|
| BLEU-1 | 0.6804 | 0.6578 |
| BLEU-2 | 0.5111 | 0.5323 |
| BLEU-3 | 0.3730 | 0.4143 |
| BLEU-4 | 0.2715 | 0.3169 |

The custom model achieved a competitive **BLEU-1** score, showing strong performance in identifying the main objects and concepts within images. BLIP performed better on higher-order BLEU metrics, which is expected due to its large-scale pretraining and stronger language modelling capabilities.

---

## 📈 Results and Visualizations

The project includes visual outputs to analyse model behaviour and performance:

- Training and validation loss curves
- Generated image captions
- Attention maps
- BLEU score comparison
- Qualitative prediction examples

These visualizations help interpret how the model learns to associate visual information with natural language.

---

## 📂 Project Structure

```text
.
├── data/
│   └── coco2017/
├── notebooks/
├── reports/
│   ├── figures/
│   └── results/
├── src/
├── models/
├── requirements.txt
└── README.md
```

---

## 🎯 Project Highlights

This project demonstrates practical experience in:

- Deep Learning
- Computer Vision
- Natural Language Processing
- Multimodal AI
- Image Captioning
- CNN-based feature extraction
- Transformer-based sequence generation
- Attention mechanisms
- BLEU evaluation
- PyTorch model training

---

## ✅ Key Outcomes

- Built a custom image captioning model using PyTorch
- Implemented a complete image and text preprocessing pipeline
- Trained an Encoder–Decoder architecture with attention
- Evaluated model performance using BLEU metrics
- Compared custom results against BLIP
- Generated visual and qualitative outputs for interpretation

---

## 📦 Installation

Install the required dependencies using:

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

Open the project notebooks:

```bash
jupyter notebook
```

Run the workflow in order, from data preparation and preprocessing to model training, evaluation, and visualisation.

------------------------------------------------------------------------

## 👨‍💻 Author

[![LinkedIn](https://img.shields.io/badge/LinkedIn-André%20Llumiquinga-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/andre-llc/)

[![GitHub](https://img.shields.io/badge/GitHub-André%20Llumiquinga-black?style=flat&logo=github)](https://github.com/andrefernandoec2608)
