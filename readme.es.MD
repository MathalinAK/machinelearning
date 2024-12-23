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

---

## Step 3: Hyperparameter Tuning
**Hyperparameter Tuning:**
- Use the fitted model and the validation set to find the optimal set of parameters where the model performs best.

---

## Step 4: Prediction
**Prediction:**
- Use the optimal set of hyperparameters from the tuning stage.
- Retrain the model with these hyperparameters using the training data.
- Use the best-fitted model to make predictions on the test data.

---

## Step 5: Test Error Rate
**Test Error Rate:**
- Compute the performance metric for your model using predictions and the actual target values from the test data.

## Bias-variance trade off:
**bias**
 	* Bias of the machine learning model is its inability to capture the true relationship the data, mathematically equal to the difference between the expectation of model and its true value
  	* It expressed as the expectation of the difference between the estimate(f(x0) and the true value.
	* Bias is a error that occur in the training data eg (if we fit and train a data in there we find an error is called bias)
** Variance:**
		- Variance of the machine learning model is the inconstancy level of model performance when applying it to different data sets.
		- When the same models that is trained using the training data performs entirely different than on test data then model variance is high.
		 - When we train a machine learning model, it learns from example data. After that, we test it on new data to see how well it works.
		- If the model does well on the training data but makes many mistakes on the new data, this difference is called variance.
		- Variance happens because the model focuses too much on the training data and doesn’t learn general patterns that work for new data.
## Bias-varaince tradeoff:
 In order to minimize the excepted test error rate, we nee to select a machine learning method that simultaneously achieves low variance and low bias
	- negative correlation between variance and bias of model.
	- Ml model flexibility has direct impact on its variance/bias.
	- If a model is more flexible, it can easily find patterns in the data, which lowers bias (fewer mistakes on the training data). But it can also overfit, making variance higher (more mistakes on new data).
	 - If a model is less flexible, it struggles to find patterns, increasing bias (more mistakes on training data). However, it is less likely to overfit, so variance decreases (fewer mistakes on new data).
	- It’s a trade-off: more flexibility means lower bias but higher variance, and less flexibility means higher bias but lower variance.
## Overfitting and regularization:
	**Underfitting:**
		- If the data has the high bias(training data)and high variance(test data)==underfitting.
	**Overfitting:**
		- bias will be low but in the testing it give high variance(testing error)this is called overfitting.




.












