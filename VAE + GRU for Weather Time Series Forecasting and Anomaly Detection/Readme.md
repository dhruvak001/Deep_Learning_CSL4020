# 🌦️ VAE + GRU for Weather Time Series Forecasting and Anomaly Detection

## 📌 Objective
This project implements:
- A **Variational Autoencoder (VAE)** for anomaly detection in weather data.
- A **Gated Recurrent Unit (GRU)** model for time series forecasting.

We use weather measurements from the Brazil Southeast region to understand and predict atmospheric changes.

---

## 📊 Dataset
- **Name:** Hourly Weather Surface - Brazil (Southeast Region)
- **Source:** [Kaggle Link](https://www.kaggle.com/datasets/PROPPG-PPG/hourly-weather-surface-brazil-southeast-region)
- **Features:** Hourly data including temperature, humidity, wind speed, and others.

---

## 🔧 Project Structure

### Part 1: Data Preparation
- ✅ **EDA**: Distributions, time series plots, missing value analysis
- ✅ **Preprocessing**: Imputation, normalization, sequence creation
- ✅ **Splits**: Train, validation, and test sets

---

### Part 2: 🔍 VAE for Anomaly Detection

#### 📐 Architecture
- Encoder and Decoder: 2 hidden layers each
- Latent dimension: Tuned based on reconstruction loss & latent space interpretability
- Loss: Reconstruction Loss + KL Divergence

#### ✅ Functionality
- Early stopping on validation loss
- Visual anomaly detection via reconstruction error
- Evaluation:
  - Precision, Recall, F1-score
  - Threshold tuning and justification
  - Latent space visualization (PCA or t-SNE)
  - Synthetic weather data generation from latent space

---

### Part 3: 🔁 GRU for Forecasting

#### ⚙️ Model Setup
- GRU-based sequence-to-sequence model
- Input: Multi-feature sequences (past `N` hours)
- Output: Forecast for next `M` hours
- Training: Batch-wise with teacher forcing (decay schedule), LR scheduler

#### 📈 Evaluation
- Metrics: MSE, MAE, RMSE
- Visualization: Predicted vs. actual trends
- Forecast Horizon Analysis
- Ablation Studies:
  - GRU vs. LSTM vs. RNN
  - Effect of input sequence length
  - Feature selection impact

---

### Part 4: 🔗 Model Integration
- Use **VAE** to filter anomalies
- Compare **GRU performance**:
  - On clean (normal) data
  - On noisy (anomalous) data
- Insights into how anomalies affect sequence forecasting models

---

## 🧪 Key Metrics

| Task                | Metric             | Description                          |
|---------------------|--------------------|--------------------------------------|
| Anomaly Detection   | Precision, Recall, F1 | Performance of VAE on detecting unusual patterns |
| Forecasting         | MSE, MAE, RMSE     | Regression quality of GRU predictions |
| Forecast Horizon    | Visualization      | How well future sequences are modeled |

---

## 🚀 Running Instructions

1. Clone the repository:
```bash
git clone https://github.com/<your-username>/DL_Assignments.git
cd DL_Assignments/Lab6
