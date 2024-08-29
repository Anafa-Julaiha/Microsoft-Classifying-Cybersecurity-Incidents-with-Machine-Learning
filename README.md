# Microsoft: Classifying Cybersecurity Incidents with Machine Learning

## Project Overview

This project focuses on classifying cybersecurity incidents into categories (TP, BP, FP) using machine learning techniques. The objective is to develop a model that can generalize well to unseen data and provide actionable insights for incident management.

## Approach

### 1. Data Exploration and Understanding
- **Initial Inspection**: Loaded `train.csv` dataset to examine its structure, including the number of features, variable types (categorical, numerical), and distribution of the target variable (TP, BP, FP).
- **Exploratory Data Analysis (EDA)**: Utilized visualizations (heatmaps, boxplots, countplots) and statistical summaries to detect patterns, correlations, and anomalies. Addressed class imbalances where necessary.

### 2. Data Preprocessing
- **Handling Missing Data**: Applied SimpleImputer to manage missing values in the dataset.
- **Feature Engineering**: Created new features from timestamps (e.g., hour of the day, day of the week) to enhance model performance.
- **Encoding Categorical Variables**: Used LabelEncoder to convert categorical features into numerical format.

### 3. Data Splitting
- **Train-Validation Split**: Divided the dataset into training and validation sets, typically using a 70-30 or 80-20 split.
- **Stratification**: Employed stratified sampling to ensure balanced class distributions in both training and validation sets.

### 4. Model Selection and Training
- **Baseline Model**: Started with a logistic regression model as a performance benchmark.
- **Advanced Models**: Experimented with RandomForestClassifier, XGBClassifier, and used RandomizedSearchCV for hyperparameter optimization.
- **Cross-Validation**: Implemented StratifiedKFold to validate model performance across different subsets of data.
- **Handling Class Imbalance**: Applied SMOTE (Synthetic Minority Over-sampling Technique) to address class imbalances and improve model performance.

### 5. Model Evaluation and Tuning
- **Performance Metrics**: Evaluated models using macro-F1 score, precision, and recall. Analyzed metrics across different classes (TP, BP, FP) for balanced performance.
- **Hyperparameter Tuning**: Fine-tuned model parameters to optimize performance.
- **Feature Importance**: Assessed feature importance using permutation importance to identify key contributing features.

### 6. Final Evaluation
- **Testing**: Evaluated the final model on the `test.csv` dataset.
- **Comparison to Baseline**: Compared test set performance with baseline results to verify consistency and improvement.

## Installation

Clone the repository and install the required packages:

```bash
git clone https://github.com/yourusername/microsoft-cybersecurity-classification.git
cd microsoft-cybersecurity-classification
pip install -r requirements.txt

