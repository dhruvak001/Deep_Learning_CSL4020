# 📦 Object Detection with DETR on Pascal VOC

## 🎯 Objective

This project implements and evaluates two **DEtection TRansformer (DETR)** variants for object detection on the **Pascal VOC** dataset:
1. **DETR with ResNet-50 backbone**
2. **DETR with Vision Transformer (ViT) backbone**

We aim to compare their performance in terms of detection quality and computational efficiency.

---

## 📚 Dataset

- **Name:** Pascal VOC
- **Link:** [http://host.robots.ox.ac.uk/pascal/VOC/](http://host.robots.ox.ac.uk/pascal/VOC/)
- **Classes:** 20 object classes (e.g., person, dog, bicycle, car)
- **Image Annotations:** XML format in VOC standard
- **Preprocessing:**
  - Resizing
  - Normalization
  - Data Augmentation (Random Flip, Color Jitter, etc.)

---

## 🧠 Model Architectures

### 📌 1. DETR with ResNet-50
- ResNet-50 pretrained backbone
- Positional encodings + Transformer encoder-decoder
- Output: Set of object queries → bounding boxes + class labels

### 📌 2. DETR with Vision Transformer (ViT)
- ViT as the backbone (patch-based input embedding)
- Token embeddings + Positional encoding
- Decoder same as DETR setup

---

## 🏋️ Training Configuration

- **Loss Function:** Hungarian loss (matching + classification + bbox loss)
- **Optimizers:** AdamW
- **Learning Rate:** 1e-4
- **Epochs:** 100+
- **Batch Size:** 16
- **Logging:** Training and validation loss

---

## 📈 Evaluation Metrics

Evaluated on Pascal VOC **test set** using:
- **mAP** (mean Average Precision)
- **AP@50**, **AP@75**
- **Precision-Recall curves**
- **F1-score**

---

## 🖼️ Visualizations

- Sample predictions on test images:
  - Ground Truth vs Predicted Boxes
  - Class confidence scores
- Training loss curves (Total Loss, Classification Loss, Bbox Loss)

---

## 🚀 How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/DL_Assignments.git
cd DL_Assignments/Lab9
