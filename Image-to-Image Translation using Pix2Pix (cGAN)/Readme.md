# 🏙️ Image-to-Image Translation using Pix2Pix (cGAN)

## 📌 Objective
This project implements and trains a **conditional Generative Adversarial Network (cGAN)** known as **Pix2Pix**, inspired by the paper:

📄 [Image-to-Image Translation with Conditional Adversarial Networks (Isola et al., 2017)](https://arxiv.org/abs/1611.07004)

The goal is to translate **label maps** of building facades into **realistic facade images** using the **CMP Facade Dataset**.

---

## 📊 Dataset

- **Dataset Name:** CMP Facade Dataset
- **Task:** Label map → Real image generation
- **Download Links:**
  - [Berkeley Pix2Pix Dataset Hub](https://efrosgans.eecs.berkeley.edu/pix2pix/datasets/)
  - [Kaggle Facades Dataset (Alternative)](https://www.kaggle.com/datasets/balraj98/facades-dataset)
- **Image Size:** Resized to `256 × 256` for training

---

## 🧠 Model Architecture

### 🔧 Generator: U-Net (Encoder-Decoder with Skip Connections)
- Downsampling path:
  - Conv → BatchNorm → LeakyReLU (x7)
- Upsampling path:
  - TransposedConv → BatchNorm → Dropout → ReLU
  - Skip connections from encoder to decoder

### 🛡️ Discriminator: PatchGAN
- Classifies each `70×70` patch in the image
- Encourages high-frequency accuracy
- Operates on concatenated input (label map + real/generated image)

---

## 🧪 Training Setup

- **Loss Functions:**
  - GAN Loss: Binary Cross Entropy
  - L1 Loss: Between real and generated image
  - Total Loss = `GAN Loss + λ * L1 Loss`, where `λ = 100`

- **Optimizer:** Adam (`β1=0.5, β2=0.999`)
- **Epochs:** 200
- **Batch Size:** 1 (as per original Pix2Pix training)
- **Learning Rate:** 2e-4

---

## 📈 Results & Visualization

- ✅ Real vs Generated Comparison
- ✅ Generator & Discriminator Loss Curves
- ✅ Side-by-side output visualization:
  - Input label map
  - Real image
  - Generated facade image

---

## 🚀 How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/DL_Assignments.git
cd DL_Assignments/Lab8
