# 🧠 Semantic Segmentation using SegNet on Pascal VOC with VGG and EfficientNet-B0 Backbones

## 📌 Objective
This project focuses on implementing the **SegNet architecture** as described in the original [SegNet paper](https://arxiv.org/pdf/1511.00561.pdf), training it on the **Pascal VOC dataset**, and evaluating its performance using multiple semantic segmentation metrics. The architecture is also extended to replace the VGG backbone with **EfficientNet-B0** to analyze the impact on efficiency and performance.

## 📚 Description

### 🔨 Architecture:
- Implementation of **SegNet** using:
  - Original **VGG-based encoder-decoder** design.
  - A custom version using a **lightweight EfficientNet-B0** encoder backbone for improved computational efficiency.
- Decoder uses pooling indices from the encoder for upsampling, following SegNet’s original design.

### 🧪 Dataset:
- **Pascal VOC 2012** dataset for object segmentation.
- Data is preprocessed and split into:
  - Training set
  - Validation set
  - Test set

### 📈 Metrics Tracked:
- Pixel-wise accuracy
- Mean Intersection over Union (mIoU)
- Dice Coefficient
- Jaccard Index
- F1 Score

### ⚙️ Training:
- Both models (VGG-based and EfficientNet-B0) are trained and evaluated under identical hyperparameter settings.
- Training progress is logged with:
  - Loss
  - Pixel accuracy

### 🔍 Comparison:
| Model Variant      | Parameters | Pixel Accuracy | Mean IoU | Dice Score | Training Time |
|--------------------|------------|----------------|----------|------------|----------------|
| SegNet (VGG)       | High       | ✅              | ✅        | ✅          | ❗ Slower       |
| SegNet (EfficientNet-B0) | Low        | ✅              | ✅        | ✅          | ✅ Faster       |

## 🚀 How to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/<your-username>/DL_Assignments.git
    cd DL_Assignments/Lab4
    ```

2. Install required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Download the Pascal VOC dataset (or link pre-downloaded path in the notebook):
    - [VOC 2012 Dataset](http://host.robots.ox.ac.uk/pascal/VOC/)

4. Run the notebook:
    ```bash
    jupyter notebook "Dhruva_Kumar_Kaushal_(B22AI017)_Lab_4_Assignment.ipynb"
    ```

## 🧪 Key Takeaways
- EfficientNet-B0 offers a lightweight alternative to VGG with comparable segmentation performance.
- Deep supervision through pooling indices enhances segmentation precision.
- mIoU and Dice scores are critical for evaluating model performance in semantic segmentation tasks.

## 🧠 Future Work
- Experiment with deeper EfficientNet variants (e.g., B1–B4)
- Use CRF post-processing for mask refinement
- Deploy segmentation in real-time applications using ONNX/TensorRT

## ✍️ Author
**Dhruva Kumar Kaushal (B22AI017)**  
Deep Learning Lab Assignment 4 — IIT Jodhpur
