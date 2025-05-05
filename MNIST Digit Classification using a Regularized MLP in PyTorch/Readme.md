# MNIST Digit Classification using a Regularized MLP in PyTorch

## Overview

This project implements a Multi-Layer Perceptron (MLP) from scratch using PyTorch for classifying handwritten digits from the MNIST dataset. It explores the effect of various regularization techniques and hyperparameter tuning on model performance and generalization.

## Features

- **Data Preprocessing**:
  - Reshaped 28x28 images into 1D vectors.
  - Applied data augmentation with random transformations (rotation, scaling, etc.).

- **MLP Architecture**:
  - Built using PyTorch with multiple linear layers.
  - Incorporated **Dropout** and **Batch Normalization** for regularization and faster convergence.
  - Applied **custom weight initialization** to improve training stability.

- **Training and Evaluation**:
  - Trained the network on the training set with cross-entropy loss.
  - Evaluated using:
    - Accuracy
    - Precision, Recall, F1-Score
    - Confusion Matrix
    - Training and validation loss analysis.

- **Regularization Analysis**:
  - Compared performance with and without dropout/batch normalization.
  - Analyzed the model's ability to reduce overfitting using visualizations and metrics.

- **Hyperparameter Tuning**:
  - Performed tuning of learning rate, batch size, dropout rate, and hidden layer size to find the optimal configuration.

## Results

- Achieved high classification accuracy on the MNIST test set.
- Observed improvement in generalization with regularization techniques.
- Demonstrated impact of hyperparameters on model stability and overfitting.

## Usage

To run the notebook:

1. Install requirements:
    ```bash
    pip install torch torchvision matplotlib scikit-learn
    ```

2. Open and run the notebook:
    ```bash
    jupyter notebook Dhruva_Kumar_Kaushal_(B22AI017)_Lab_1_Assignment.ipynb
    ```

## File Structure

- `Dhruva_Kumar_Kaushal_(B22AI017)_Lab_1_Assignment.ipynb`: Main notebook with code, results, and analysis.

## Author

- **Dhruva Kumar Kaushal** – B22AI017 – IIT Jodhpur

## License

This project is part of a lab assignment and is intended for academic purposes only.
