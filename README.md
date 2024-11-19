# Image Classification with Enhanced Pretrained Models

This project focuses on image classification using **MobileNetV2** as a baseline and demonstrates performance enhancement through advanced techniques such as **data augmentation**, **Batch Normalization**, **Dropout**, and **fine-tuning**.

---

## 📋 Project Overview

The goal of this project is to classify images into three categories:
- **Canteen**
- **Library**
- **Open Space**

### Key Objectives:
1. Build a **baseline model** using MobileNetV2 pretrained on ImageNet.
2. Enhance the baseline model by adding layers and techniques to improve performance and generalization.
3. Compare the results of the baseline and enhanced models using validation accuracy and loss.

---

## 📂 Dataset

### Initial Dataset:
- Total of **150 images** (50 images per class).

### Augmented Dataset:
- After applying **data augmentation**, the dataset size increased to **740 training images**.
- Augmentation techniques used:
  - **Rotation** (up to 30 degrees)
  - **Shifting** (width and height, up to 20%)
  - **Shearing** (up to 20%)
  - **Zooming** (±20%)
  - **Horizontal Flipping**
  - **Brightness Adjustment** (80%–120%)

### Final Dataset:
- **Training Set**: 740 images
- **Validation Set**: 151 images

---

## 🛠️ Methods

### Baseline Model:
- **Architecture**: MobileNetV2 with pretrained weights from ImageNet.
- **Modifications**:
  - Global Average Pooling (GAP) layer.
  - Dense layer with 3 output classes and `softmax` activation.
- **Training**:
  - Frozen base layers.
  - Trained for 10 epochs.
  - Validation Accuracy: **78.15%**

### Enhanced Model:
- **Enhancements**:
  - Added **Batch Normalization** and **Dropout** layers.
  - Introduced a fully connected dense layer with ReLU activation.
  - Fine-tuned the last 30 layers of MobileNetV2.
- **Training**:
  - Initial training for 15 epochs.
  - Fine-tuning for 10 epochs with a reduced learning rate.
  - Validation Accuracy: **92.05%**

---

## 📊 Results

| **Metric**             | **Baseline Model** | **Enhanced Model** |
|-------------------------|--------------------|--------------------|
| **Training Accuracy**   | 99.2%             | 99.9%             |
| **Validation Accuracy** | 78.15%            | 92.05%            |
| **Validation Loss**     | 0.5914            | 0.2252            |

---

## 🚀 How to Run the Project

### 1. Clone the Repository:
```bash
git clone https://github.com/yourusername/your-repo-name.git
