# 🎭 WGAN-Based Synthetic Face Generation and Evaluation using CelebA

## 📌 Objective
This project implements:
- A **Wasserstein GAN (WGAN)** to generate synthetic face images.
- A **CNN classifier** to compare classification performance between real and synthetic datasets using the **"Young"** attribute.

---

## 📊 Dataset
- **Name:** CelebA Dataset
- **Source:** Available directly via `torchvision.datasets`
- **Images:** 202,599 face images
- **Labels:** 40 attributes per face, including "Young"

---

## 🔧 Project Structure

### Part 1: 🧹 Data Preparation
- ✅ Loaded CelebA dataset using PyTorch
- ✅ Resized images to `3 x 64 x 64`
- ✅ Normalized pixel values to [-1, 1]
- ✅ Split into `train`, `val`, and `test` sets

---

### Part 2: 🧪 WGAN for Synthetic Image Generation

#### 🧠 Architecture
- **Generator & Critic (Discriminator)**: DCGAN-based blocks with spectral normalization
- **Latent vector (z):** Sampled from standard Gaussian

#### 📉 Training & Evaluation
- Trained with **Wasserstein Loss with Gradient Penalty**
- Plotted:
  - Generator loss
  - Discriminator loss
- Evaluated using:
  - **Inception Score (IS)**
  - **Fréchet Inception Distance (FID)**

---

### Part 3: 🧬 Hyperparameter Tuning
- Experimented with:
  - Learning rate: `1e-4`, `2e-4`, `5e-5`
  - Batch size: `64`, `128`
  - Latent vector size: `100`, `128`, `256`
- Compared generated samples before & after tuning

---

### Part 4: 🔍 Train CNN Classifier on Real Data
- Trained a CNN binary classifier on **"Young"** vs **"Old"** faces
- Architecture: 3 conv layers + FC head
- Validated using real validation split

---

### Part 5: 🏷️ Annotate Synthetic Data
- Generated `0.7 × len(train_data)` synthetic samples using the WGAN Generator
- Used CNN classifier from Part 4 to annotate each image with **"Young"/"Old"** label

---

### Part 6: 🧪 CNN Classifier on Mixed Dataset
- Training Set: `70% synthetic + 30% real` images
- Evaluated final classifier on test set

#### 🧾 Reported Metrics
| Metric     | Description                          |
|------------|--------------------------------------|
| Accuracy   | Overall correct classification       |
| Precision  | True Positives / Predicted Positives |
| Recall     | True Positives / Actual Positives    |
| F1-score   | Harmonic mean of Precision & Recall  |

---

## 📈 Results

- **WGAN generated realistic face samples after tuning**
- **FID and IS improved with hyperparameter optimization**
- **Classifier trained on real+synthetic data achieved comparable accuracy to real-only baseline**

---

## 🚀 Running Instructions

1. Clone the repository:
```bash
git clone https://github.com/<your-username>/DL_Assignments.git
cd DL_Assignments/Lab7
