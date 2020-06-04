# Wine-Quality-Prediction
## Abstract
### Problem
1. Which physiochemical features are most relevant in determining the quality of wine? And are they different for red and white?
2. And are the difference signficiant based on classical, bootstrap, and Bayesian method?
3. Predict the quality scores of wine
### Conclusion
1. Quality of wine is more correlated (corr>0.2) with the following features: alcohol, density, volatile acidity, and chlorides. 
And we found that the top 2 features (alcohol and density) are significantly different between red and white wines based on bootstrap hypothesis testing.
2. PCA was used to narrow down model input features. 'pH' and'sulphates' were deemed not significant.
3. Quality scores of wine were then predicted using the following models
  - Multivariant linear regression: The RMSE is 1.39 (~20% of the target mean), meaning that the model can make general good prediction, but is not very accurate
  - Naive Bayes model: The RMSE is 1.02 which is better than the RMSE from the multivariant linear regression model. However the accuracy score is only 0.413
  - Gradient Boosting Classifier: The RMSE is 0.6375, about half that of the other two models. Since the LightGBM model gave us the lowest RMSE, this model should be used to make prediction of wine quality.
