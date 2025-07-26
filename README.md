# PCA Comparison on Digits Dataset with Logistic Regression

This repository contains Python code that compares **Exact PCA** and **Approximate PCA (Randomized SVD)** on the popular handwritten digits dataset. The project demonstrates dimensionality reduction followed by classification using logistic regression, highlighting differences in accuracy and computational speed between the two PCA methods.

---

## Overview

- Loads the `digits` dataset (8x8 pixel images of handwritten digits 0-9).
- Splits data into training (80%) and test (20%) sets.
- Standardizes features to zero mean and unit variance.
- Performs dimensionality reduction to 2 components using:
  - Exact PCA (`svd_solver='full'`)
  - Approximate PCA (`svd_solver='randomized'`)
- Trains logistic regression classifiers on:
  - The full feature set (no PCA)
  - Exact PCA-reduced features
  - Approximate PCA-reduced features
- Compares classification accuracy and PCA computation times.
- Visualizes training data projected onto the first two principal components using approximate PCA.

---

## Installation

This code requires Python 3 and the following Python packages:

- numpy
- matplotlib
- scikit-learn

You can install dependencies with:

```bash
pip install numpy matplotlib scikit-learn
