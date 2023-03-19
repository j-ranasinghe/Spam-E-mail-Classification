# Spam Email Classification using KNN and Decision Tree

[![Python Version](https://img.shields.io/badge/python-3.7%20%7C%203.8%20%7C%203.9-blue)](https://www.python.org/downloads/release/python-394/)
[![KNN](https://img.shields.io/badge/KNN-Nearest%20Neighbors-yellow)](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)
[![Decision Tree](https://img.shields.io/badge/Decision%20Tree-Classifier-green)](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html)
[![PCA](https://img.shields.io/badge/PCA-Dimensionality%20Reduction-orange)](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html)

---

This repository contains code for spam email classification using KNN and Decision Tree algorithms. 

---
## Python Versions

The code in this repository was written and tested using Python 3.9.16. 

---
## Dataset

The dataset used in this project is the [UCI Machine learning repository - Spambase dataset](https://archive.ics.uci.edu/ml/datasets/Spambase). The last column of 'spambase.data' denotes whether the e-mail was considered spam (1) or not (0). Most of the attributes indicate whether a particular word or character was frequently occuring in the e-mail.

---
## Key Features

### PCA

Since the email data had a high number of features, PCA (Principal Component Analysis) was used to reduce the dimensionality of the data. PCA is a technique that transforms the data into a lower-dimensional space while preserving the most important information. 

### Cross-validation

To evaluate the performance of the models, we used cross-validation. We used k-fold cross-validation, where the data is divided into k subsets and each subset is used as the validation set k times. The average performance across all k folds is then used as the final performance metric.

### Model Evaluation

Trained the two models on the preprocessed and PCA-reduced data: KNN (k-nearest neighbors) and Decision Tree. Then evaluated the performance of each model using cross-validation and calculated the following metrics:

* Accuracy: the proportion of correctly classified emails

* Precision: the proportion of predicted spam emails that were actually spam

* Recall: the proportion of actual spam emails that were correctly classified as spam

* F1 score: the harmonic mean of precision and recall

It was found that both models performed well on the dataset, with KNN achieving an accuracy of 0.91 and Decision Tree achieving an accuracy of 0.89. 

