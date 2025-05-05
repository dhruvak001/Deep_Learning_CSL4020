# 🔁 Transfer Learning from STL-10 to MNIST using CNNs in PyTorch

## 📌 Objective
Implement a **transfer learning pipeline** where a convolutional neural network (CNN) is first **pre-trained on the STL-10 dataset** and then **fine-tuned on the MNIST dataset** under various transfer settings. The goal is to explore how knowledge learned from a rich source domain (STL-10) can be adapted to a simpler target domain (MNIST).

## 📚 Description

### 🔨 Workflow:

1. **Dataset Preprocessing**:
    - STL-10 and MNIST are both:
        - Normalized
        - Resized to consistent input shape
        - Augmented (STL-10: stronger; MNIST: mild or none)
    - DataLoaders are prepared for train, validation, and test splits.

2. **Pretraining Phase**:
    - A CNN model (custom or pre-trained on STL-10) is trained.
    - Training metrics such as **loss** and **accuracy** are logged.

3. **Transfer Learning Techniques**:
    - **Strategy 1:** Freeze CNN feature extractor, train only linear layers.
    - **Strategy 2:** Freeze initial few CNN layers; train the rest.
    - **Strategy 3:** Fine-tune the **entire network** end-to-end.

4. **Evaluation** on MNIST:
    - Overall Accuracy
    - Per-Class Precision, Recall, and F1 Score
    - Confusion Matrix Visualization

### 🧪 Metrics Used:
| Metric                  | Purpose                              |
|-------------------------|--------------------------------------|
| Accuracy                | Overall classification performance   |
| Precision (per class)   | Class-specific error rate control    |
| Recall (per class)      | True positive capture rate           |
| F1 Score                | Balance of precision & recall        |
| Confusion Matrix        | Misclassification analysis           |

### 🧠 STL-10 vs. MNIST
- STL-10 is a more complex dataset (color, natural images).
- MNIST is grayscale and simpler.
- This makes it a suitable testbed for assessing **knowledge transfer**.

## 🚀 How to Run

1. Clone the repository:
    ```bash
    git clone https://github.com/<your-username>/DL_Assignments.git
    cd DL_Assignments/Lab5
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Download datasets:
    - STL-10: [https://cs.stanford.edu/~acoates/stl10/](https://cs.stanford.edu/~acoates/stl10/)
    - MNIST: Automatically downloaded using `torchvision.datasets.MNIST`.

4. Run the notebook:
    ```bash
    jupyter notebook "Dhruva_Kumar_Kaushal_(B22AI017)_Lab_5_Assignment.ipynb"
    ```

## 🔍 Comparative Results

| Transfer Method        | Accuracy | Avg. F1 Score | Notes                        |
|------------------------|----------|---------------|------------------------------|
| Linear Head Only       | ✅        | ✅             | Fast, less flexible          |
| Partial Layer Training | ✅✅       | ✅✅            | Balanced trade-off           |
| Full Fine-Tuning       | ✅✅✅      | ✅✅✅           | Best performance, more time  |

## 💡 Insights
- Even with domain shift (color vs. grayscale), meaningful features are transferable.
- Freezing lower layers saves compute with minimal accuracy loss in some cases.
- Full fine-tuning yields best results but requires careful learning rate tuning.

## ✍️ Author
**Dhruva Kumar Kaushal (B22AI017)**  
Deep Learning Lab Assignment 5 — IIT Jodhpur
