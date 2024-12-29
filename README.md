Name: VEDIKA SULE

Company: CODTECH IT SOLUTION

ID: CT08FGJ

Domain: DATA ANALYTICS

Duration: December 2024 to January 2025

Mentor: N. SANTHOSH

OVERVIEW OF PROJECT

PROJECT: EXPLORATORY DATA ANALYSIS (EDA) OF IRIS DATASET


#OBJECTIVE:

The goal of this project is to analyze the Iris dataset, which contains measurements of flowers, such as:
Sepal Length
Sepal Width
Petal Length
Petal Width

It also includes the variety (species) of the flowers. The objective is to:

Understand the patterns and trends in the data.

Analyze how features like petal and sepal measurements are distributed.

Study relationships between these features.

Detect unusual data points (outliers) and understand how features are related to each other.


#KEY ACTIVITIES:

Loading and Checking the Data:

The dataset is loaded using Python's pandas library.

Key information like column types, statistical summaries, and missing values is checked.


Feature Distribution Analysis:

Histograms are created to visualize how the features (e.g., petal length, sepal width) are spread out in the data.


Correlation Analysis:

A heatmap is used to show how strongly the numerical features (e.g., petal length and sepal length) are related to each other.


Outlier Detection:

Box plots help in identifying any extreme or unusual values in the data.


Feature Relationships:

Scatter plots are used to study relationships between specific features like sepal length vs. sepal width.

A pair plot is created to explore all feature relationships grouped by flower species (variety).


#TECHNOLOGY USED:

Python Libraries:

Pandas: To handle and analyze the data.

NumPy: For mathematical operations.

Matplotlib: To create basic visualizations.

Seaborn: To create more advanced, attractive charts and plots.

 
Visualization Techniques:

Histograms, scatter plots, heatmaps, box plots, and pair plots are used to make the data easier to understand.


Dataset:

The Iris Dataset, a well-known dataset in machine learning, includes measurements of flowers and their species (Setosa, Versicolor, and Virginica). It is widely used for classification tasks.


CODE

/* TASK1 */
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

iris=pd.read_csv("iris_dataset.csv")

print(iris.info())
print(iris.describe())
print(iris.isnull().sum())

# Ploting histograms for numeric columns.
iris.hist(figsize=(10,9), bins=20, color='skyblue', edgecolor='black')
plt.suptitle('FEATURE DISTRIBUTION', fontsize=15)
plt.show()

# Correlation Analysis.
plt.figure(figsize=(10, 8))
sns.heatmap(correlation_matrix, annot=True, cmap='pink', fmt=".2f")
plt.title("Correlation Matrix")
plt.show()

# Outlier Detection.
plt.figure(figsize=(10,8))
sns.boxplot(data=iris.iloc[:,:-1], palette='Set3')
plt.title('Box Plot for Outlier Detection', fontsize=15)
plt.show()

# Feature Relationships.
sns.scatterplot(data=iris, x='sepal.length', y='sepal.width', hue='variety', palette='Set2')
plt.title('Sepal Length vs Sepal Width', fontsize=14)
plt.show()
pairplot = sns.pairplot(iris, hue='variety', diag_kind='kde', palette='Set2')
pairplot.fig.suptitle('Feature Relationships', y=1.02, fontsize=16) 
plt.show()


OUTPUT:

   ![Screenshot (137)](https://github.com/user-attachments/assets/0b901ee2-b933-4b12-a38a-793c52f65a1f) 
   ![Screenshot (138)](https://github.com/user-attachments/assets/c23456fb-ee78-42b9-a2c2-f46594f4f2d9)
   ![Screenshot (139)](https://github.com/user-attachments/assets/dac20574-7192-4db0-a4e1-808ab9b1e9ad)
   ![Screenshot (141)](https://github.com/user-attachments/assets/6442f62c-6262-4242-bec5-c0e1809ecaac)


