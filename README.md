# KNN Classification

  

This project aims to apply the K-Nearest Neighbors (KNN) algorithm for data classification, with the main goal of understanding how the algorithm functions. The project includes exploratory analysis, KNN application, validation techniques, hyperparameter optimization, and visualization of decision boundaries.

  

![Cartão de Visita](https://cdn.discordapp.com/attachments/1167606494536142864/1167606533811601429/Copia_de_Modern_Creative_Business_Card.png?ex=654ebd52&is=653c4852&hm=78a86e0bfea405ba39b4970117881fee3e14aefb38b23db2ad685b7a785f6708&)

  

## Table of Contents

- [1. Introduction](#1-Introduction)

- [2. Data Understanding](#2-Data-Understanding)

- [3. Action Plan](#3-Action-Plan)

- [4. Data Insights](#4-Data-Insights)

- [5. Machine Learning Metrics](#5-Machine-Learning-Metrics)

- [6. Results](#6-Results)

- [7. Conclusion](#5-Conclusion)
  
  

## 1. Introduction
This project aims to carry out a comprehensive **exploratory analysis** of the classic dataset, which will serve as the basis for implementing the **KNN (K-Nearest Neighbors)** algorithm. The dataset in question is **Wine**, which is widely recognized and available in the **[UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/109/wine)**, **[Scikit Learning](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html#sklearn.datasets.load_wine)** and also on **[Kaggle](https://www.kaggle.com/datasets/tawfikelmetwally/wine-dataset/data)**. Although it is a simple dataset, designed mainly for studies and does not present a specific problem, it is possible to apply data analysis techniques, extract insights and knowledge in a similar way to what would be done in more complex and problematic datasets.neighbors.
  

## 2. Data Understanding

The Wine dataset consists of 14 features, one of which is the target, and 178 labels. All the data is numerical, with no missing values or duplicates. The nomenclature dictionary includes:

  

| Attribute                      | Definition                         | Data Type |
| ------------------------------ | -----------------------------------| --------- |
| alcohol                        | Alcohol content                    | float64   |
| malic_acid                     | Malic acid                         | float64   |
| ash                            | Ash                                | float64   |
| alcalinity_of_ash              | Alkalinity of ash                  | float64   |
| magnesium                      | Magnesium                          | float64   |
| total_phenols                  | Total phenols                      | float64   |
| flavanoids                     | Flavanoids                         | float64   |
| nonflavanoid_phenols           | Non-flavanoid phenols              | float64   |
| proanthocyanins                | Proanthocyanins                    | float64   |
| color_intensity                | Color intensity                    | float64   |
| hue                            | Hue                                | float64   |
| od280/od315_of_diluted_wines   | OD280/OD315 of diluted wines       | float64   |
| proline                        | Proline                            | float64   |
| class                          | Wine type (target)                 | int32     |

  

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

  

* Flavanoids show a strong correlation with other features, especially with Total Phenols (0.86) and OD280/OD315 of diluted wines (0.79).

* However, the lowest correlation occurs with the target variable (Class), with a coefficient of -0.85.

* The Proline feature stands out as providing the best separation between classes, especially for class 0.

* The color_intensity also stands out, especially when combined with Flavanoids and Total Phenols.

* It was observed that the data is on significantly varied scales. This disparity is evident in summaries, analyses, and distribution plots.

* The lowest value found is in Nonflavanoid Phenols (0.13).

* Considering the wide range of scales, the application of techniques like PCA (Principal Component Analysis) may be beneficial for reducing the dimensionality of the data, allowing for more effective and accurate analysis.

  

## 5. Machine Learning Metrics
As the only Machine Learning model used is KNN (K = 5), I chose to use the data in two states (Normalized and Standardized) for comparison purposes.  With the following results:

| Scale        | Accuracy | Precision | Recall | F1-Score |
| ------------ | -------- | --------- | ------ | -------- |
| Normalized   | 100%     | 100%      | 100%   | 100%     |
| Standardized | 97.56%   | 98%       | 98%    | 98%      |



## 6. Results

**General**
*   Both normalization and standardization had an accuracy above 95% in the test and training sets. This information could mean that:
    *   Overfitting
	*   Size of the test set
	*   Good separability
	*   Proper pre-processing
	*   Appropriate choice of hyperparaters
	
	
**Overfitting**
*   100% accuracy on the test set can be an indication of overfitting. Overfitting occurs when the model fits the training data so well that it does not generalize well to new data, i.e. the model "overlearns" the training data and is unable to generalize to previously unseen data. The fact that KNN has perfect accuracy on the test set suggests that it is memorizing the training data rather than finding general patterns.
	
**Size of the test set**
*   It may be that the test set is small, and, by coincidence, the examples in it are very well represented by the nearest neighbors in KNN. This can lead to 100% accuracy on the test set, but it doesn't necessarily mean that the model is optimal.
	
**Good separability**
*   If the data in the test set is easily separable, KNN can work very well, since it relies on the proximity of neighbors to make predictions. If the test examples are well spread out and the groups are clearly distinct, KNN is more likely to achieve high accuracy.

**Proper pre-processing**
*   Proper data pre-processing can lead to improved model performance. If the training and test data have been properly normalized, treated to eliminate outliers and prepared appropriately, this can contribute to improved performance.

**Appropriate choice of hyperparameters**
*   KNN's hyperparameters, such as the number of neighbors (k), can significantly affect the model's performance. The appropriate choice of hyperparameters is fundamental. It is important to check that the hyperparameters have been adjusted appropriately to avoid overfitting.

## 7. Conclusion
The exploratory analysis undertaken in this data science project has provided valuable insights into the classification of our dataset, employing a primary focus on the K-Nearest Neighbors (KNN) algorithm. To maintain simplicity and avoid introducing overly advanced techniques, the analysis concludes at this juncture with a descriptive emphasis.

In Section 8, we observed consistent classifications in both datasets, with variations primarily attributed to the distance in our visualization from the graph. While achieving commendable precision and accuracy, it is imperative to acknowledge the necessity for model refinement to mitigate overfitting and enhance overall generalization.

To bolster the model's adaptability to previously unobserved data, it is recommended to delve into advanced techniques. This includes exploring strategies such as hyperparameter tuning, cross-validation, and meticulous feature selection. By doing so, we aim to fortify the robustness of our model, ensuring that its performance transcends a mere adaptation to the training data and instead represents a more steadfast capability to handle new instances. These considerations are pivotal in constructing a dependable and effective model for classifying real-world data.

It is essential to recognize the limitations of our data set, acknowledging its small size compared to real-world data.  Despite this, the insights gained and good practices exercised during this exploratory phase lay the groundwork for future studies. In conclusion, this project serves as a valuable exercise in understanding classification techniques, with the potential for extrapolation and application to larger datasets and real-world scenarios.
