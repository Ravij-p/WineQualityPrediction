

---

# Wine Quality Prediction

This project uses machine learning to predict the quality of red wine based on various physicochemical properties. The dataset used is the Wine Quality dataset, which includes 1599 instances and 12 attributes.

## Files

- `winequality-red.csv`: The dataset containing the physicochemical properties and quality ratings of red wines.
- `WineQualityPrediction.ipynb`: Jupyter Notebook containing the data analysis, visualization, and model training code.

## Data Description

The dataset contains the following columns:

- `fixed acidity`
- `volatile acidity`
- `citric acid`
- `residual sugar`
- `chlorides`
- `free sulfur dioxide`
- `total sulfur dioxide`
- `density`
- `pH`
- `sulphates`
- `alcohol`
- `quality`: The quality rating of the wine (0 to 10)

## Project Overview

1. **Data Loading and Exploration**
    - Load the data using pandas.
    - Display the first few rows of the data.
    - Check for missing values.

2. **Data Visualization**
    - Plot the count of each quality rating.
    - Visualize the relationship between `volatile acidity` and `quality`.
    - Generate a heatmap to show correlations between different features.

3. **Data Preprocessing**
    - Separate features (X) and the target variable (y).
    - Binarize the quality variable: 1 for good quality (quality >= 7), 0 for bad quality.

4. **Model Training**
    - Split the data into training and testing sets.
    - Train a Random Forest Classifier on the training data.

5. **Model Evaluation**
    - Calculate and print the accuracy on training and testing data.
    - Use the trained model to make a prediction on a sample input.

## Random Forest Algorithm

Random Forest is an ensemble learning method that constructs multiple decision trees during training and outputs the mode of the classes (classification) or mean prediction (regression) of the individual trees. It is known for its robustness and high accuracy, handling both classification and regression tasks effectively.

### Key Steps in Random Forest:

1. **Bootstrap Sampling**: Random subsets of the training data are sampled with replacement to create multiple datasets.
2. **Decision Trees**: For each dataset, a decision tree is trained.
3. **Random Feature Selection**: At each split in the decision tree, a random subset of features is considered.
4. **Aggregation**: Predictions from all the trees are aggregated to determine the final output.

### Advantages:

- Handles large datasets efficiently.
- Reduces overfitting by averaging multiple trees.
- Works well with both numerical and categorical data.

### Disadvantages:

- Can be computationally intensive.
- Interpretability is lower compared to single decision trees.

## Model Performance

- **Training Accuracy**: 100%
- **Testing Accuracy**: 93.44%

The Random Forest model achieved high accuracy on both training and testing data, indicating its effectiveness in predicting wine quality based on the provided features.

---
