# 🧠 CNN Classification with Depth-Wise Separable Convolutions and Dense Blocks on CIFAR-10

## 📌 Objective
This project involves the implementation of a custom Convolutional Neural Network (CNN) architecture that utilizes **depth-wise separable convolutions** and **dense blocks** to improve computational efficiency and classification accuracy on the CIFAR-10 dataset.

## 📚 Description

### 🔨 Architecture Highlights:
- The CNN comprises **four dense blocks** to promote feature reuse and efficient gradient flow.
- All convolution operations use **depth-wise separable convolutions**:
  - **Depth-wise Convolution:** Applies a single filter per input channel.
  - **Point-wise Convolution:** Uses 1×1 convolutions to combine outputs across channels.

### 🧪 Comparison:
- The performance and computational efficiency of **depth-wise separable convolutions** are compared to **traditional convolutional layers**.

### 🧠 Evaluation Metrics:
- Accuracy
- Precision
- Recall
- F1-Score

### 📈 Training Configuration:
- Dataset: **CIFAR-10**
- Epochs: **Minimum 100** or until the loss stabilizes
- Framework: **PyTorch**

## ⚙️ Technologies Used
- Python 3.x
- PyTorch
- NumPy
- Matplotlib
- scikit-learn (for metrics)

## 📊 Results & Observations
- Plotted training & validation loss/accuracy curves
- Computed metrics: Accuracy, Precision, Recall, F1-Score
- Benchmarked runtime and memory use of:
  - Traditional Conv2D layers
  - Depth-wise Separable Convolutions
- Analyzed trade-offs in efficiency vs accuracy

## 🚀 How to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/<your-username>/DL_Assignments.git
    cd DL_Assignments/Lab3
    ```

2. Install required packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Open and run the notebook:
    ```bash
    jupyter notebook "Dhruva Kumar Kaushal (B22AI017) - Lab 3 Assignment.ipynb"
    ```

## 📌 Notes
- Depth-wise separable convolutions offer a significant reduction in the number of parameters and computational cost.
- Dense blocks enable better feature propagation and alleviate vanishing gradient problems.

## ✍️ Author
**Dhruva Kumar Kaushal (B22AI017)**  
Deep Learning Lab Assignment 3 — IIT Jodhpur
