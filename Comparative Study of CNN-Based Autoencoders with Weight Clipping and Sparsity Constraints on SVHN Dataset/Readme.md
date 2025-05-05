# 📌 Comparative Study of CNN-Based Autoencoders with Weight Clipping and Sparsity Constraints on SVHN Dataset

## 🧠 Objective
This project involves designing and evaluating CNN-based autoencoders for image reconstruction on the SVHN dataset using PyTorch. The key objective is to analyze the effect of different regularization strategies on model performance.

## 📚 Description
Two autoencoders are implemented and compared:

1. **Autoencoder A**:
   - Loss Function: Mean Squared Error (MSE)
   - Regularization: All weights clipped to the range [-0.5, 0.5]

2. **Autoencoder B**:
   - Same setup as Autoencoder A
   - Additional **L1 sparsity constraint** added to encourage sparse activations

Both models are trained under identical conditions to ensure fair comparison.

### 🔧 Training Details
- Dataset: SVHN (Street View House Numbers)
- Epochs: Minimum 100 or until convergence
- Regularization: Weight Clipping (both), L1 Sparsity (model B only)
- Evaluation: PSNR (Peak Signal-to-Noise Ratio), MSE
- Hyperparameters tuned:
  - Activation functions: ReLU, LeakyReLU, Tanh
  - Optimizers: Adam, SGD

## 📦 Technologies Used
- Python 3.x
- PyTorch
- NumPy
- Matplotlib
- scikit-learn (for evaluation metrics)

## 📈 Results
- Loss curves and PSNR scores for both models are plotted and analyzed.
- Visual comparison of reconstructed vs original images.
- Observations on how regularization affects overfitting, convergence, and image fidelity.

## 🚀 How to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/<your-username>/DL_Assignments.git
    cd DL_Assignments/Lab2
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the Jupyter notebook:
    ```bash
    jupyter notebook "Dhruva Kumar Kaushal (B22AI017) - Lab 2 Assignment.ipynb"
    ```

## 📊 Evaluation Metrics
- **MSE (Mean Squared Error)**
- **PSNR (Peak Signal-to-Noise Ratio)**
- **L1 Sparsity Measure** (for Autoencoder B)

## ✍️ Author
**Dhruva Kumar Kaushal (B22AI017)**  
Deep Learning Lab Assignment 2 — IIT Jodhpur
