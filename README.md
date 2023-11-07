# KNN Classification

This project aims to apply the K-Nearest Neighbors (KNN) algorithm for data classification, with the main goal of understanding how the algorithm functions. The project includes exploratory analysis, KNN application, validation techniques, hyperparameter optimization, and visualization of decision boundaries.

![Cartão de Visita](https://cdn.discordapp.com/attachments/1167606494536142864/1167606533811601429/Copia_de_Modern_Creative_Business_Card.png?ex=654ebd52&is=653c4852&hm=78a86e0bfea405ba39b4970117881fee3e14aefb38b23db2ad685b7a785f6708&)

## Table of Contents
- [1. Introduction](#1-Introduction)
- [2. Data Understanding](#2-Data-Understanding)
- [3. Action Plan](#3-Action-Plan)
- [4. Data Insights](#4-Data-Insights)
- [5. Future Outlook](#5-Future-Outlook)


## 1. Introduction

This project utilizes the K-Nearest Neighbors (KNN) algorithm to classify data from the **Wine dataset**. KNN is a machine learning technique that categorizes a data point based on the nearest points in a multidimensional space. In the context of the Wine dataset, which contains chemical information about wines, KNN will be applied to categorize wines into different groups. The data is available on [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/109/wine), [Kaggle](https://www.kaggle.com/datasets/tawfikelmetwally/wine-dataset/data) e [Scikit Learn](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html#sklearn.datasets.load_wine).
 

## 2. Data Understanding
The Wine dataset consists of 14 features, one of which is the target, and 178 labels. All the data is numerical, with no missing values or duplicates. The nomenclature dictionary includes:

|Attribute|Definition|Data Type|
|---|---|---|
|alcohol|Alcohol content|float64|
|malic_acid|Malic acid|float64|
|ash|Ash|float64|
|alcalinity_of_ash|Alkalinity of ash|float64|
|magnesium|Magnesium|float64|
|total_phenols|Total phenols|float64|
|flavanoids|Flavanoids|float64|
|nonflavanoid_phenols|Non-flavanoid phenols|float64|
|proanthocyanins|Proanthocyanins|float64|
|color_intensity|Color intensity|float64|
|hue|Hue|float64|
|od280/od315_of_diluted_wines|OD280/OD315 of diluted wines|float64|
|proline|Proline|float64|
|class|Wine type (target)|int32|

## 3. Action Plan

### 3.1. Objective
After completing the [initial KNN implementation project](https://github.com/lfaferreira/ada-potencia-tech-knn-project), I was intrigued to deepen my understanding of how KNN works. This repository explores the capabilities of the KNN algorithm in detail, with a focus on classification and improving understanding.

### 3.2. Tools and Frameworks
Scope of tools used in the project:

- Python 3.11.5
- Jupyter Notebook
- Git & GitHub
- Kaggle
- Pandas
- Numpy
- Machine Learning Classification Model (KNN)

## 4. Data Insights

*   Flavanoids show a strong correlation with other features, especially with Total Phenols (0.86) and OD280/OD315 of diluted wines (0.79).
*   However, the lowest correlation occurs with the target variable (Class), with a coefficient of -0.85.
*   The Proline feature stands out as providing the best separation between classes, especially for class 0.
*   The color_intensity also stands out, especially when combined with Flavanoids and Total Phenols.
*   It was observed that the data is on significantly varied scales. This disparity is evident in summaries, analyses, and distribution plots.
*   The lowest value found is in Nonflavanoid Phenols (0.13).
*   Considering the wide range of scales, the application of techniques like PCA (Principal Component Analysis) may be beneficial for reducing the dimensionality of the data, allowing for more effective and accurate analysis.

## 5. Future Outlook
* Add machine learning metrics and selected filters.
* Add project results.
* Include a project conclusion.