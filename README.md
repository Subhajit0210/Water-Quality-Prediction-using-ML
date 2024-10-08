# Water Quality Prediction

A machine learning project designed to predict water potability based on various physical and chemical characteristics. This project leverages advanced data analysis and machine learning techniques to provide insights into water quality, using a dataset with multiple water quality parameters.

## Table of Contents

- [Project Overview](#project-overview)
- [Key Objectives](#key-objectives)
- [Dependencies](#dependencies)
- [Data Collection](#data-collection)
- [Data Preparation](#data-preparation)
- [Data Visualization](#data-visualization)
- [Classification Techniques](#classification-techniques)
- [Modeling and Evaluation](#modeling-and-evaluation)
- [Results and Insights](results-and-insights)
- [Usage](#usage)
- [Contributing](#contributing)

## Project Overview

Ensuring water quality is critical for public health and safety. This project aims to classify water samples as potable or non-potable using a dataset comprising various indicators of water quality. By applying multiple machine learning algorithms, this project seeks to accurately predict water potability and understand the factors that most significantly affect water quality.

## Key Objectives

- **Predict Potability**: Use machine learning models to classify water samples as potable (safe to drink) or non-potable based on a set of features such as pH, hardness, solids, chloramines, and more.
- **Feature Analysis**: Understand the influence of different water quality parameters on potability, offering insights into which features are most indicative of water quality.
- **Model Evaluation**: Implement and compare multiple machine learning algorithms to determine the most effective model for predicting water quality, ensuring robustness and accuracy.

## Dependencies
The project requires the following Python libraries:
- numpy
- pandas
- matplotlib
- seaborn
- scipy
- scikit-learn

## Data Collection
The dataset utilized in this project is `water_potability.csv`, which includes the following features:

- **pH**: A measure of how acidic/basic water is.
- **Hardness**: The amount of dissolved calcium and magnesium in the water.
- **Solids**: The total dissolved solids in ppm (parts per million).
- **Chloramines**: The concentration of chloramines in ppm.
- **Sulfate**: The amount of sulfate in ppm.
- **Conductivity**: Electrical conductivity of the water in μS/cm.
- **Organic Carbon**: The total organic carbon content in ppm.
- **Trihalomethanes**: Concentration of trihalomethanes in μg/L.
- **Turbidity**: The cloudiness or haziness of the water.
- **Potability**: A binary variable indicating whether the water is safe to drink (1) or not (0).

## Data Preparation

The data preparation steps included:

- **Loading the data**: The dataset was loaded into a Pandas DataFrame for manipulation and analysis.
- **Exploratory Data Analysis (EDA)**: Conducted to understand the distribution and relationships between different water quality features.
- **Handling Missing Values**: Checked for missing values in the dataset and imputed missing entries for `ph`, `Sulfate`, and `Trihalomethanes` with their respective mean values to ensure data completeness.
- **Feature Scaling**: Applied standardization using `StandardScaler` to normalize the features, which is crucial for algorithms sensitive to feature magnitudes.
- **Data Splitting**: The dataset was split into training and testing sets to evaluate model performance on unseen data.
- **Data Visualization**: Created a heatmap to visualize the correlation matrix, helping identify the strength of relationships between variables.

## Data Visualization

To gain insights into the water quality data, several visualizations were created using various types of charts:

1. **Distribution of pH Levels**:
   - **Histogram**: Used to visualize the distribution and skewness of pH levels in the water samples. This helps identify the range of acidity and alkalinity present in the dataset.

2. **Distribution of Hardness**:
   - **Histogram**: Created to observe the variation in water hardness across different samples, which is essential for understanding the concentration of calcium and magnesium.

3. **Distribution of Solids**:
   - **Histogram**: Plotted to analyze the range and distribution of total dissolved solids, offering insights into water quality and its impact on potability.

4. **Distribution of Chloramines**:
   - **Histogram**: Displayed to understand the levels of chloramines used as disinfectants in the water samples, a key factor in determining water safety.

5. **Correlation Heatmap**:
   - **Heatmap**: Created to visualize the correlation between different water quality features, helping identify which features are closely related and highlighting potential multicollinearity that could affect model performance.

6. **Scatter Plots**:
   - **Scatter Plot**: Used to examine the relationship between pairs of features, providing a visual representation of how two variables correlate with each other.

7. **Pair Plot**:
   - **Pair Plot**: Generated to visualize the distribution of individual features and relationships between multiple pairs of features in a single figure, helping to identify patterns and potential correlations.

8. **Linear Regression Plot (lmplot)**:
   - **Lmplot**: Used to display linear relationships between features, incorporating a regression line to show the trend, which helps in understanding linear dependencies in the dataset.

9. **Box Plot**:
   - **Box Plot**: Created to visualize the spread and presence of outliers in each feature. This is useful for understanding the variability within the data and identifying potential outliers that might need handling before model training.

These visualizations were essential in understanding the dataset's characteristics, guiding the feature selection process, and preparing the data for modeling.

## Classification Techniques
The following machine learning classification algorithms were used in this project:
- **Gaussian Naive Bayes**:

Gaussian Naive Bayes is a probabilistic classifier based on Bayes' theorem, assuming that features follow a Gaussian distribution. This algorithm is particularly useful for classification problems with continuous input variables. It is simple, easy to implement, and works well with a small dataset. In this project, Gaussian Naive Bayes helps in understanding the probabilistic distribution of water quality features.

- **Decision Tree Classifier**:

Decision Tree Classifier is a non-parametric supervised learning method used for classification. It works by splitting the data into subsets based on the value of input features. This model is easy to interpret and visualize, making it valuable for understanding feature importance in the dataset. Decision trees are prone to overfitting, but they provide a good baseline and insight into which features are most impactful.

- **Random Forest Classifier**:

Random Forest is an ensemble learning method that combines multiple decision trees to improve predictive accuracy and control overfitting. By averaging the results of several trees, Random Forest mitigates the risk of overfitting that comes with individual decision trees. It is robust and handles both numerical and categorical data well. In this project, Random Forest is used for its superior performance in dealing with high-dimensional data and its ability to provide feature importance.

- **Logistic Regression**:

Logistic Regression is a linear model commonly used for binary classification problems. It estimates the probability of a binary response based on one or more predictor variables. Despite its simplicity, logistic regression can be surprisingly effective for linearly separable data and is often used as a baseline model in classification tasks. It provides coefficients for each feature, offering insights into their influence on the potability of water.

## Modeling and Evaluation
Each algorithm was trained and evaluated using a consistent set of metrics to ensure comparability:

- **Accuracy**: The proportion of true results among the total number of cases examined.
- **Precision, Recall, and F1-score**: Metrics that provide insights into the performance of the classification model, especially in cases of imbalanced classes.
- **Confusion Matrix**: A table used to describe the performance of a classification model by comparing predicted and actual labels.

## Results and Insights
The results section in the notebook details the performance of each model. Generally, the Random Forest Classifier provided the highest accuracy and robustness across various metrics, suggesting it as the most effective model for this task. Comprehensive evaluation and insights are provided in the notebook.

## Usage
To run the project, follow these steps:
1. Clone the repository:
```bash
git clone https://github.com/yourusername/water-quality-prediction.git
```
2. Navigate to the project directory:
```bash
cd water-quality-prediction
```
3. Run the Jupyter notebook:
```bash
jupyter notebook Water-Quality-Prediction.ipynb
```

## Contributing
Contributions are welcome! Please create a new branch for any changes and submit a pull request for review.
