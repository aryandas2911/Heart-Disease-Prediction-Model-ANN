# ❤️ Heart Disease Prediction using Artificial Neural Network

This project builds a **Deep Learning model** to predict whether a patient has heart disease using clinical data.  
The model is implemented using **TensorFlow/Keras** and trained on the **UCI Heart Disease Dataset**.

The goal is to demonstrate a **complete machine learning pipeline** including:

- Data exploration
- Feature analysis
- Data preprocessing
- Neural network training
- Model evaluation

The trained model predicts the **probability of heart disease** based on patient medical attributes such as age, chest pain type, cholesterol level, and maximum heart rate.

---

## Kaggle Notebook

Full implementation available on Kaggle:

https://www.kaggle.com/code/aryandas29/heart-disease-prediction-model-ann

---

## Problem Type

Binary Classification

| Target Value | Meaning |
|--------------|--------|
| 0 | No Heart Disease |
| 1 | Heart Disease |

The model outputs a **probability score between 0 and 1** using a sigmoid activation function.

---

## 📊 Dataset

The model is trained using the **Heart Disease Dataset** available on Kaggle.

Dataset link:  
https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset

The dataset originates from the **UCI Machine Learning Repository** and was compiled from four medical databases:

- Cleveland
- Hungary
- Switzerland
- Long Beach V

Although the original dataset contains **76 attributes**, most machine learning experiments use **14 important clinical features**, including the target variable representing the presence of heart disease.

---

### Dataset Size

| Property | Value |
|--------|------|
| Total Samples | 1025 |
| Features | 13 |
| Target Variable | 1 |

---

### Target Distribution

The dataset is relatively balanced.

| Class | Count |
|------|------|
| Heart Disease (1) | 526 |
| No Heart Disease (0) | 499 |

Balanced classes help the model avoid bias toward one category.

---

### Key Features

Some important clinical features used by the model include:

| Feature | Description |
|------|-------------|
| age | Age of the patient |
| cp | Chest pain type |
| trestbps | Resting blood pressure |
| chol | Serum cholesterol |
| thalach | Maximum heart rate achieved |
| exang | Exercise induced angina |
| oldpeak | ST depression caused by exercise |
| ca | Number of major vessels |

These features represent **cardiovascular indicators commonly used in medical diagnosis**.

---

## 🔎 Exploratory Data Analysis

Exploratory Data Analysis was performed to understand feature distributions and identify relationships between clinical variables and heart disease.

Key observations from the analysis:

- **Chest pain type (`cp`)** and **maximum heart rate (`thalach`)** showed strong positive correlation with heart disease presence.
- **Exercise-induced angina (`exang`)** and **ST depression (`oldpeak`)** were strong negative indicators.
- Traditional risk metrics like **cholesterol** and **resting blood pressure** showed weaker separation between classes in this dataset.

Visualizations used during analysis:

- Correlation heatmap
- Boxplots for continuous variables vs target
- Countplots for categorical features vs target

These insights helped confirm that several cardiovascular indicators provide meaningful signals for training the neural network classifier.

---

## 🧠 Model Architecture

An **Artificial Neural Network (ANN)** was built using **TensorFlow/Keras** to perform binary classification.

### Network Structure

Input Layer → Dense → Dropout → Dense → Output


---

## 📈 Results

After training the Artificial Neural Network, the model was evaluated on the test dataset to measure its predictive performance.

### Model Performance

| Metric | Score |
|------|------|
| Training Accuracy | ~98% |
| Test Accuracy | ~85% |

The model demonstrates strong predictive capability, indicating that neural networks can effectively learn patterns from clinical heart disease data.

### Evaluation

Performance was assessed using:

- Accuracy score
- Confusion matrix
- Training vs validation loss curves

The model shows **good generalization with minimal overfitting**, making it effective for binary heart disease classification.

### Prediction Output

The model outputs a **probability score between 0 and 1**:

- Values closer to **1 → Higher risk of heart disease**
- Values closer to **0 → Lower risk**
