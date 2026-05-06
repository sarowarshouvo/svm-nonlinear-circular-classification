# svm-nonlinear-circular-classification

# Nonlinear Classification of Circular Data Using Support Vector Machines

## 📘 Overview
This repository contains the implementation and analysis for **Mini Project 3** of **MATH 5384 – Advanced Machine Learning**.

The project investigates how different Support Vector Machine (SVM) kernels perform on a nonlinear circular dataset consisting of concentric inner and outer circles. The study compares linear, polynomial, and Radial Basis Function (RBF) kernels while analyzing underfitting, overfitting, and decision boundary behavior.

Special attention is given to kernel selection, model complexity, symmetry effects, and generalization performance.

---

## 🎯 Objectives

- Study nonlinear classification using Support Vector Machines
- Compare linear, polynomial, and RBF kernels
- Analyze the effect of polynomial degree
- Investigate the impact of RBF gamma values
- Examine underfitting and overfitting behavior
- Visualize nonlinear decision boundaries
- Compare training and testing misclassification errors

---

## 📊 Dataset Description

A synthetic circular dataset was generated using concentric circles.

### Inner Circle

- Radius approximately 1
- Represents Class 0

### Outer Circle

- Radius approximately 3
- Represents Class 1

The coordinates were generated using:

```math
x_1 = r\cos(\theta), \quad x_2 = r\sin(\theta)
```

where:

- \( r \) represents radius
- \( \theta \) represents random angles between \(0\) and \(2\pi\)

Small Gaussian noise was added to create realistic circular structures.

---

## 🧠 Models Evaluated

### 1. Linear Kernel SVM

A baseline linear classifier:

- Unable to separate concentric circles
- Produces high training and testing errors
- Demonstrates severe underfitting

---

### 2. Polynomial Kernel SVM

Polynomial degrees tested:

```math
d \in \{2,5,7,10\}
```

Key observations:

- Even-degree kernels preserve circular symmetry
- Odd-degree kernels distort the boundary
- Degree 2 achieves perfect classification
- Degree 10 shows slight overfitting

---

### 3. RBF Kernel SVM

Gamma values tested:

```math
\gamma \in \{10,30,100\}
```

Key observations:

- Moderate gamma values generalize well
- High gamma creates overly complex boundaries
- Gamma = 100 causes overfitting

---

## 📈 Key Findings

- Linear SVM completely fails on circular data
- Even-degree polynomial kernels perform significantly better
- Degree 2 polynomial kernel achieves zero testing error
- Moderate RBF gamma values achieve perfect classification
- Large gamma values overfit the training data
- Kernel choice must align with data geometry

---

## 🛠️ Technologies Used

- Python
- NumPy
- Scikit-learn
- Matplotlib

---

## 📂 Repository Structure

```text
├── svm_circular_classification.ipynb
├── MiniProject3_SVM_Report.pdf
├── figures/
├── README.md
└── requirements.txt
```

---

## ▶️ How to Run

```bash
pip install -r requirements.txt
jupyter notebook
```

Run the notebook:

```text
svm_circular_classification.ipynb
```

---

## 📎 Included Contents

- Circular dataset generation
- Linear kernel SVM
- Polynomial kernel SVM experiments
- RBF kernel SVM experiments
- Decision boundary visualizations
- Error comparison plots
- Underfitting and overfitting analysis

---

## 👤 Author

**Saroar Jahan Shuba**  
M.S. Computational & Quantitative Methods  
Lamar University
