# Lung Cancer Prediction

This project demonstrates what I learned in Data Science at Georgia Tech’s Bootcamp: https://dsgtbootcamp.netlify.app/schedule. 

1.	## Proposal
### Introduction
Using symptoms as predictors, can predict the presence of lung cancer using machine learning classification?

### Motivation
Machine learning and AI is widely used for medical applications and is an active area of research. I am interested in machine learning applications to medicine, and this is a specific task which assisted in understanding machine learning.

### Plan of action
-	Explore and inspect the data.
-	Study the example notebook: https://www.kaggle.com/code/abdallahwagih/lung-colon-cancer-cnn-98-6 
-	Implement own study using it as inspiration. Incorporate own changes and document learning.

### How will success be measured?
If we can obtain a similar accuracy to the example (98%~).

### How will the data be collected?
We will use the public dataset from Kaggle: https://www.kaggle.com/datasets/mysarahmadbhat/lung-cancer 

2.	## Exploratory Data Analysis
### How was the dataset explored?
The dataset was first inspected for an overview, such as the variables’ data types, then screened for common issues such as trailing spaces, null, and duplicate values.
Summary statistics of the data was then obtained, and data visualization was performed to gain insights. 
The dataset was explored for distributions, outliers, correlations, class imbalances.
Various methods to quantify multicollinearity were explored, including heatmap, variance inflation factor, and eigenvalues.

### What were the most important aspects of the dataset found from exploratory data analysis?
The most important aspect of the dataset was the class imbalance and the multicollinearity in the predictor variables.

### How did the findings of the exploratory data analysis influence the project’s direction?
The exploration of the dataset influenced the direction of the project by researching methods to deal with the issues.

3.	## Data Preprocessing
### How was your dataset preprocessed? What were the predominant techniques used and why?
-	Encoding was used for categorical variables.
-	Scaling of columns was performed.
-	Duplicates were dropped and column names were stripped, basic data cleaning.
-	Imbalanced data was handled with oversampling of the minority class.
-	To handle multicollinearity, PCA was explored. Ridge Regression is another option.
-	The primary goal is prediction, so multicollinearity was not directly addressed in the final model, but instead focused on evaluation metrics more relevant to the task (Recall).

4.	## Machine Learning

### What models did your team choose to solve the problem at hand with your preprocessed dataset? 

Models used:
-	Decision Tree Classifier
-	Logistic Regression
-	(Multi-Layer Perceptron) Neural Network
-	Linear Support Vector Machine
-	Kernel Support Vector Machine

Followed by optimization with oversampling of the minority class.

Models used: 
-	K Neighbors Classifier
-	Kernel Support Vector Machine
-	Logistic Regression
-	Random Forest Classifier
-	Gradient Boosting Classifier

Evaluation Metric:

Metric: Recall
Recall = TruePositives / (TruePositives + FalseNegatives)
Recall is the best metric because here were are concerned about reducing False Negatives. I.e. measuring how many Lung Cancer Patients were missclassified as Non Lung Cancer.

Kernel Support Vector Machine was found to be the best model for this task, based on the evaluation metric.

Evaluation:

Recall - 97%
Accuracy - 98%
It has only two (FP) misclassifications for class 1.
AUC - 0.9831

### What are plans for further action based on the models?
I would like to try more techniques to handle multicollinearity: PCA and Ridge Regression or other regularization techniques.

### References:
Dataset: https://www.kaggle.com/datasets/mysarahmadbhat/lung-cancer  
Data Science at Georgia Tech Bootcamp: https://dsgtbootcamp.netlify.app/  
IBM Multicollinearity: https://www.ibm.com/topics/multicollinearity  
Hex Detecting and Remedying Multicollinearity: https://hex.tech/blog/detecting-and-remedying-multicollinearity/  
Lung Cancer Prediction Kaggle Notebook: https://www.kaggle.com/code/casper6290/lung-cancer-prediction-98
