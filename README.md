## Deep Learning Lab Assignments Repository

This repository contains **nine** comprehensive deep learning lab assignments completed by **Dhruva Kumar Kaushal (B22AI017)** at IIT Jodhpur. Each assignment focuses on a different aspect of deep learning, from basic neural networks to advanced generative models and transformer‑based architectures.

---

## Table of Contents

1. [Lab 1: MNIST Digit Classification with MLP](#lab-1-mnist-mlp)  
2. [Lab 2: CNN Autoencoder with Sparsity on SVHN](#lab-2-cnn-autoencoder-svhn)  
3. [Lab 3: Depth‑Wise Separable CNN on CIFAR‑10](#lab-3-depthwise-cnn-cifar10)  
4. [Lab 4: SegNet for Semantic Segmentation (Pascal VOC)](#lab-4-segnet-pascal-voc)  
5. [Lab 5: Transfer Learning STL‑10 → MNIST](#lab-5-transfer-learning)  
6. [Lab 6: VAE + GRU for Weather Forecasting & Anomaly Detection](#lab-6-vae-gru-weather)  
7. [Lab 7: WGAN Synthetic Data + CNN Classification on CelebA](#lab-7-wgan-celeba)  
8. [Lab 8: Pix2Pix Image‑to‑Image Translation (CMP Facade)](#lab-8-pix2pix)  
9. [Lab 9: DETR Object Detection on Pascal VOC](#lab-9-detr)  

---

### Lab 1: MNIST Digit Classification with MLP
**Path:** `Lab1/Dhruva_Kumar_Kaushal_(B22AI017)_Lab_1_Assignment.ipynb`  
Implement a Multi‑Layer Perceptron in PyTorch for classifying MNIST digits. Includes data augmentation, dropout, batch normalization, custom weight initialization, hyperparameter tuning, and evaluation metrics (accuracy, precision, recall, F1, confusion matrix).

### Lab 2: CNN Autoencoder with Sparsity on SVHN
**Path:** `Lab2/Dhruva Kumar Kaushal (B22AI017) - Lab 2 Assignment.ipynb`  
Design two CNN autoencoders for SVHN: one with weight clipping and one with additional L1 sparsity constraint. Compare reconstruction quality via PSNR and analyze the effect of activation functions and optimizers.

### Lab 3: Depth‑Wise Separable CNN on CIFAR‑10
**Path:** `Lab3/Dhruva Kumar Kaushal (B22AI017) - Lab 3 Assignment.ipynb`  
Build a CNN with four dense blocks using depth‑wise separable convolutions. Train on CIFAR‑10 and evaluate accuracy, precision, recall, F1, and compare computational efficiency against traditional convolutions.

### Lab 4: SegNet for Semantic Segmentation (Pascal VOC)
**Path:** `Lab4/Dhruva_Kumar_Kaushal_(B22AI017)_Lab_4_Assignment.ipynb`  
Implement SegNet (VGG‑based) and a lightweight variant with EfficientNet‑B0 backbone. Train on Pascal VOC, log pixel accuracy and loss, and evaluate mIoU, Dice score, and Jaccard Index.

### Lab 5: Transfer Learning STL‑10 → MNIST
**Path:** `Lab5/Dhruva_Kumar_Kaushal_(B22AI017)_Lab_5_Assignment.ipynb`  
Pre‑train a CNN on STL‑10 and transfer to MNIST via three strategies: train only head, freeze initial layers, and fine‑tune all layers. Evaluate with accuracy, per‑class metrics, and confusion matrices.

### Lab 6: VAE + GRU for Weather Forecasting & Anomaly Detection
**Path:** `Lab6/Dhruva Kumar Kaushal (B22AI017) - Lab 6 Assignment.ipynb`  
Use a Variational Autoencoder for detecting anomalies in Brazilian weather data and a GRU network for multi‑step forecasting. Analyze VAE reconstruction errors, latent space, and evaluate GRU forecasting (MSE, MAE, RMSE) including ablation studies.

### Lab 7: WGAN Synthetic Data + CNN Classification on CelebA
**Path:** `Lab7/Dhruva Kumar Kaushal (B22AI017) - Lab 7 Assignment.ipynb`  
Train a Wasserstein GAN on CelebA faces, evaluate with Inception Score and FID, then train a binary CNN classifier (“Young” vs “Old”) on real, synthetic, and mixed datasets, reporting standard classification metrics.

### Lab 8: Pix2Pix Image‑to‑Image Translation (CMP Facade)
**Path:** `Lab8/Dhruva Kumar Kaushal (B22AI017) - Lab 8 Assignment.ipynb`  
Implement Pix2Pix cGAN for label‑to‑facade translation using a U‑Net generator and PatchGAN discriminator. Train on the CMP Facade dataset and visualize results alongside loss curves.

### Lab 9: DETR Object Detection on Pascal VOC
**Path:** `Lab9/Dhruva_Kumar_Kaushal_(B22AI017)_Lab_9_Assignment.ipynb`  
Compare DETR variants with ResNet‑50 and Vision Transformer backbones on Pascal VOC. Train transformer encoder‑decoder object detector, evaluate mAP, AP50, AP75, precision‑recall, and F1 scores.

---

## Installation & Usage
1. **Clone the repository**  
   ```bash
   git clone https://github.com/dhruvak001/DL_Assignments.git
   cd DL_Assignments
