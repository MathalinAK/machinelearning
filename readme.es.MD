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






.












