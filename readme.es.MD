## Machine learning 
- It is a brand of artificial intelligence.
- That helps to build models based on the data and learn the data in order to make different decision.
- ex: They are using in any industries like healthcare entertainment in order to improve the customer behaviour.
## Supervised vs unsupervised
- Supervised(the primary goal of supervised learning is minimize errors in predictions)
- Requires training data with independent variable(labelled data)
- Need labelled data to supervise the algorithm when learning from the data.
- Ex: Regression models ,classification models.
## Unsupervised learning:
- Requires training data with independent variables only.
- No need labelled data that can supervise the algorithm when learning from the data
- Ex: Clustering models, Outlier detection models.
Supervised is categories into two methods depending on the type of dependent variable they are predicted.
## Regression and classification 
 1. Regression:
	 *  Regression predict the continuous values
	 * It can be used when the response variable to be predicted is a continuous variable
	 * ex: linear regression, fixed effects regression, xgboost regression(identify the temperature based on the give feature)
	 *  For regression the means squared is commonly used
2. Classification:
	* while the classification predict the categorized values.  
	* It can be used when the response variable to be predicted is a continuous variable
	* ex :logistic regression, xgboost classification(will rain or not?)
	* for classification the accuracy commonly used .
## classification performance metrics:
- Accuracy =Classification/CorrectPrediction + IncorrectPrediction
- Precision =TruePositive/TruePositive+ FalsePositive
- Recall=TruePositive/TruePositive+ falsegative
- F1Score = 2*Recall + Precision/Recall + Precision
## Clustering performance metrices:
* homogeneity
* silhouette score
* completeness
## Machine Learning model evalution:
 # Machine Learning Model Evaluation

## Step 1: Preparing the Data
**Data Preparation:**
- Split the data into **training**, **validation**, and **test** sets.
- The training set is used to train the model.
- The validation set is used to optimize hyperparameters and pick the best model.
- The test set is used to evaluate the model's performance.

---

## Step 2: Model Training
**Model Training:**
- Choose an algorithm or a set of algorithms for the task.
- Train the model on the training data and save the fitted model.
- The choice of algorithm depends on the specific task and the characteristics of the data.
## Step 3: Hyperparameter Tuning
**Hyperparameter Tuning:**
- Use the fitted model and the validation set to find the optimal set of parameters where the model performs best.
## Step 4: Prediction
**Prediction:**
- Use the optimal set of hyperparameters from the tuning stage.
- Retrain the model with these hyperparameters using the training data.
- Use the best-fitted model to make predictions on the test data.
## Step 5: Test Error Rate
**Test Error Rate:**
- Compute the performance metric for your model using predictions and the actual target values from the test data.

# Bias-Variance Tradeoff

## Bias
- **Bias** in a machine learning model is its inability to capture the true relationship in the data.
- Mathematically, it is equal to the difference between the expectation of the model and the true value.
- It is expressed as the expectation of the difference between the estimate (`f(x₀)`) and the true value.
- Bias is an error that occurs in the **training data**.  
  *Example:* If we train a model on data and it fails to capture the true patterns, the error is called bias.

---

## Variance
- **Variance** measures the inconsistency of the model's performance across different datasets.
- If the model performs well on the training data but poorly on the test data, the model has high variance.
- High variance occurs when the model focuses too much on the training data and fails to generalize to new data.
- **Explanation:**
  - When a model learns from the training data, it picks up patterns.
  - If it learns overly specific patterns (overfitting), it performs poorly on new data.
  - This difference in performance between training and new data is called variance.

---

## Bias-Variance Tradeoff
- To minimize the expected test error rate, we need a machine learning method that simultaneously achieves **low bias** and **low variance**.
- There is a **negative correlation** between variance and bias:
  - A **flexible model** can easily capture patterns in data, reducing bias but increasing variance (overfitting).
  - A **less flexible model** may fail to capture patterns, increasing bias but reducing variance (underfitting).
- **Key Idea**: 
  - More flexibility → Lower bias, higher variance.
  - Less flexibility → Higher bias, lower variance.
## Overfitting and Regularization

### Underfitting:
- Occurs when:
  - The model has **high bias** on training data.
  - The model has **high variance** on test data.
- Results in poor performance on both training and test datasets.

### Overfitting:
- Occurs when:
  - The model has **low bias** on training data.
  - The model has **high variance** on test data (large testing error).
- Happens when the model is too focused on the training data and fails to generalize.
- variance(testing error)this is called overfitting.
### Overfitting Reduction Techniques:
- **Reduce Model Complexity**: Use fewer parameters or apply regularization (L1/L2).  
- **Collect More Data**: More data reduces the chance of overfitting.  
- **Resampling (Cross-Validation)**: Train and test on different subsets to identify overfitting.  
- **Early Stopping**: Stop training when performance on a validation set starts decreasing.  
- **Ensemble Methods**: Combine multiple models (e.g., decision trees) to reduce overfitting.  
- **Dropout**: A regularization technique that drops random neurons during training in neural networks.

### Generalization:
- **Low Bias + Low Variance**: The model predicts well with minimal residuals (errors). This indicates good generalization.

### Regularization:
- **Definition**: Shrinks some coefficients towards zero to penalize unimportant variables and reduce overfitting.  
  - **Purpose**: Introduces small bias to decrease variance and solve overfitting.  
  - **Techniques**:  
    - **Ridge Regression**: Uses L2 norm.  
    - **Lasso Regression**: Uses L1 norm.  
    - **Dropout**: Used in neural networks.  
- **Dropout**: A neural network technique that randomly removes some neurons during training to prevent overfitting.

- **Ridge Regression (L2 Regularization)**: Shrinks coefficients towards 0 to reduce model variance using the L2 norm (Euclidean distance).

- **Lasso Regression (L1 Regularization)**: Shrinks some coefficients to 0, removing irrelevant features, using the L1 norm.

- **Dependent Variable**: The measured or tested variable, dependent on the independent variable.

- **Independent Variable**: The variable controlled or manipulated, believed to affect the dependent variable.

- **Statistical Significance**: An effect unlikely to occur by chance, considered real.

- **Linear Regression**: Models the relationship between variables:
  - **Simple Linear Regression**: One independent variable.
  - **Multiple Linear Regression**: Multiple independent variables.
## simple linear regression:
## y=B0 + B1X + U
- **y (Dependent Variable)**: The variable being measured or predicted.  
- **X (Independent Variable)**: The variable that influences or explains y.  
- **B0 (Intercept)**: The constant, unknown term where the regression line crosses the y-axis.  
- **Beta (B1)**: The slope coefficient, an unknown parameter that shows the impact of X on y.  
- **U (Error Term)**: The difference between the predicted and actual values (unexplained part).  
- **i (Index)**: Represents each observation (row) in the dataset.

### Multiple Linear Regression:
- A statistical method to model the relationship between a dependent variable (y) and multiple independent variables (X1, X2, ... Xn).

### Linear Regression Estimation:
- **Goal**: To estimate the unknown parameters (B0, B1, ...) to understand how X impacts y.  
- **Ordinary Least Squares (OLS)**:  
  - A technique to estimate parameters by finding the line that minimizes the sum of squared errors.  
  - Fits a regression line through paired x and y values to best predict y from X. 
### Importing Libraries:

- **import pandas as pd**: Used for reading and manipulating data (e.g., dataframes, handling missing values, and preprocessing).  

- **import numpy as np**: Used for numerical operations, working with arrays, and data manipulation.  

- **import matplotlib.pyplot as plt**: Used for creating visualizations like scatter plots, line plots, and heatmaps.  

- **import seaborn as sns**: Used for advanced data visualization, such as scatter plots and heatmaps.  

- **from scipy import stats**: Provides tools for statistical analysis, including tests and probability distributions.  

- **import statsmodels.api as sm**: Used for statistical modeling like linear regression and time series analysis.  

- **from sklearn.linear_model import LinearRegression**: Used to create and train linear regression models.  

- **from sklearn.model_selection import train_test_split**: Splits the data into training and testing sets for model evaluation.  
### Missing Data Analysis:

- **Check for Missing Values**:
  - missing_values = data.isnull().sum(): Count missing values in each column.
  - Calculate the percentage of missing data:
 	- missing_percentage = (missing_values / len(data)) * 100
    

- **Handling Missing Data**:
  - If the missing data is not important to the project, use the percentage of missing data to decide:
    - **Drop Independent Variable**: If only a small percentage of data is missing in an important column, keep the column and drop observations with missing values (e.g., in the total_bedrooms column).
    - **Imputation**: Replace missing values systematically using mean, median, or model-based imputation techniques.

- **When to Drop or Impute**:
  - If 10% of data is missing in a large dataset, you can drop the missing rows.
  - If 20%-40% of data is missing in a smaller dataset, consider imputing the missing values.

- **Remove Rows with Missing Values**:
  - Use `data_cleaned = data.dropna()` to remove rows with missing values.
  - Verify removal with -->print(data_cleaned.isnull().sum()).

---

### Data Exploration and Visualization:

- **Understand Data**:
  - Look for patterns, differences, imbalances, and categorical values.

- **Use data.describe()**:
  - Provides descriptive statistics like mean, standard deviation, and percentiles.

- **Percentiles**:
  - **25th Percentile (Q1)**: Lower quartile.
  - **50th Percentile (Q2)**: Median.
  - **75th Percentile (Q3)**: Upper quartile.
Data Visualization and Histogram (Matplotlib, Seaborn)
- Visualize the dependent variable (target or response variable) to understand its distribution.  
- In this case, the dependent variable is the **Median House Values**.
1. **Understand the Distribution**:
   - Analyze how the Median House Values are distributed across the dataset.
   - Identify the most frequently appearing median house values.
   - Identify blocks with unique or less frequently appearing median house values.
   
2. **Insights from the Histogram**:
   - The histogram shows the number of occurrences (frequency) of each median house value.
   - Focus on:
     - Values that appear most often.
     - Values that appear less often.
   - Keep only the **most relevant and representative data points** for analysis.

## Quantiles and Percentiles
Quantiles and percentiles help summarize the data distribution and provide deeper insights:
- Quantiles divide the data into equal-sized intervals.
  - Example: Quartiles split the data into 4 equal parts.
- Percentiles** show the relative standing of a value within the data.
----
**Correlation:** Measures the linear relationship between two variables. It ranges from:
- 1: Perfect positive correlation.
- 0: No correlation.
- -1: Perfect negative correlation.

###  Dropping a Column in a DataFrame

- **`data.drop()`**: Removes the specified column.
- **`"total_bedrooms"`**: The name of the column to be dropped.
- **`axis=1`**: Indicates that the operation is performed on columns.
- **`data =`**: Reassigns the updated DataFrame to the same variable to apply the change.
- **`data.columns`**: Returns a list of column names in the updated DataFrame.
- **Purpose**: This helps verify the removal of the specified column.

# **Data Analysis and Cleaning Steps**

## **Boxplot for Removing Outliers**
Boxplots are a statistical visualization tool that help identify outliers and understand data distribution. They represent the data using the following components:

### **Components of a Boxplot**
- **Central Box**: Represents the interquartile range (IQR), which includes the middle 50% of the data.
- **Bottom Edge**: Indicates the 25th percentile (Q1).
- **Top Edge**: Indicates the 75th percentile (Q3).
- **Length of the Box**: Represents the IQR (`Q3 - Q1`).
- **Median Line**: The dark line within the box represents the median (middle value) of the dataset when sorted in ascending order.
- **Whiskers**:
  - Lines extending from the box indicate the range of the dataset, excluding outliers.
  - Whiskers span from the **Lower Bound** (`Q1 - 1.5 × IQR`) to the **Upper Bound** (`Q3 + 1.5 × IQR`).
- **Outliers**: Data points outside this range are represented as black dots.

---

## **Removing Outliers**
To remove outliers, follow these steps:

1. **Calculate**:
   - **IQR**: `Q3 - Q1`
   - **Lower Bound (LB)**: `Q1 - 1.5 × IQR`
   - **Upper Bound (UB)**: `Q3 + 1.5 × IQR`

2. **Filter the Data**:
   - Include only observations within the bounds:
     ```
     LB ≤ median income ≤ UB
     ```
   - This process results in clean data without extreme values.

---

## **Identifying High Income and Common Values**
To analyze the data:
- **Define**: Common prices and areas for houses.
- **Find Patterns**: Frequently appearing data and patterns, particularly for people with average income.

---

## **Correlation Heatmaps**
A correlation heatmap visualizes pairwise correlation scores between variables. Correlation values range from:
- **-1**: Strong negative correlation.
- **0**: No correlation.
- **1**: Strong positive correlation.

### **Key Elements**
- **White Areas**: Indicate strong negative correlations.
- **Dark Green Areas**: Indicate strong positive correlations.
- **Diagonal Line**: Contains values of 1 as they represent the correlation of each variable with itself.
- **Mirrored Values**: The heatmap is symmetric around the diagonal.

### **Purpose**
- Identify problematic independent variables with high correlation (**multicollinearity**).
  - Multicollinearity distorts regression models.
- Decide which variables to drop based on frequent high correlations.
  - **Example**: Drop variables like `total_bedrooms` if they show high correlation with other independent variables.

---

## **Transforming String Values to Numeric (Dummy Variables)**
- **Dummy Variables**: Binary (0 or 1) representations of categorical data.
  - **Example**: `ocean_proximity` with five categories is converted into five dummy variables (e.g., `inland`, `island`, `nearby`).
  - If all dummy variables for a category are 0, it indicates the condition is not satisfied.
- **Purpose**: Helps analyze the statistical impact of categorical features on the dependent variable (e.g., median house values).

---

## **Identifying Significant Features**
To determine which features significantly impact the dependent variable (e.g., median house values):
- Analyze features describing houses (e.g., size, location, number of rooms) that influence the target variable.

---

## **Splitting Data: `train_test_split`**
- Use `train_test_split` to divide the data:
  - **80%**: Training data
  - **20%**: Test data
- **Random State**: Ensures reproducibility of results.

---

## **Fitting Models**
1. **Train the Model**:
   - Use both dependent (Y) and independent (X) variables:
     ```python
     model.fit(X_train, Y_train)
     ```

2. **Make Predictions**:
   - Use the trained model to make predictions on unseen data:
     ```python
     Y_pred = model.predict(X_test)
     ```

3. **Evaluate Performance**:
   - Compare predictions (`Y_pred`) with actual values (`Y_test`).

4. **Analyze Results**:
   - Predict and analyze median house values based on the fitted model and unseen data.










.












