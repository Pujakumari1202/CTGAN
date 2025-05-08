## 🧠 Enhancing Classifier Accuracy on Imbalanced Datasets using CTGAN


# 📖 About the Project
This project addresses the challenge of class imbalance in classification problems by comparing traditional machine learning performance before and after synthetic data augmentation.

Initially, we trained three classifiers — Support Vector Machine (SVM), Decision Tree (DT), and K-Nearest Neighbors (KNN) — on an imbalanced version of the Dry Bean Dataset. As expected, the models showed lower accuracy due to the skewed class distribution.

We first attempted to balance the dataset using a standard GAN (Generative Adversarial Network), but the generated data did not align well with tabular classification requirements and led to poor results.

To overcome this, we used CTGAN (Conditional Tabular GAN), a model specifically designed for generating synthetic tabular data while preserving feature distributions and class relationships. This significantly improved model performance:

SVM: +5% accuracy

Decision Tree: +7% accuracy

KNN: +6% accuracy

This demonstrates the importance of choosing domain-specific generative models like CTGAN when working with structured data.



## 📊 Dataset
We used the Dry Bean Dataset from the UCI Machine Learning Repository:

Features: 16 numerical attributes (e.g., Area, Perimeter, Compactness)

Target: Type of Bean (7 classes)

The dataset was imbalanced, making it ideal for studying the effect of synthetic oversampling techniques.



## ✨ Features
Evaluation of ML models (SVM, DT, KNN) on imbalanced data

Attempted oversampling using vanilla GAN (unsuccessful)

Successful augmentation using CTGAN

Detailed comparison of model performance before and after augmentation



## 🛠️ Tech Stack
Language: Python

Libraries:

        scikit-learn (SVM, DT, KNN, metrics)

        pandas, numpy, matplotlib, seaborn (data processing & visualization)

        ctgan (for synthetic data generation)



## 📁 Project Structure

```bash
project/
│
├── CTGANLast.ipynb         # Full implementation and results
├── results/                # Accuracy plots and confusion matrices (optional)
├── README.md
└── requirements.txt        # Python dependencies
```


## 🚀 How to Run
1) Open CTGANLast.ipynb in Jupyter or Colab.

2) Run all cells sequentially:

            Fetch and preprocess the dataset

            Train baseline models (SVM, DT, KNN)

            Use CTGAN to generate synthetic data

            Retrain models on the balanced dataset

3) Observe accuracy improvements and plots.




## 📈 Results Summary
| Model         | Accuracy (Before) | Accuracy (After CTGAN) | Improvement |
| ------------- | ----------------- | ---------------------- | ----------- |
| KNN           | 92%               | 98%                    | +6%         |
| SVM           | 93%               | 98%                    | +5%         |
| Decision Tree | 89%               | 96%                    | +7%         |



