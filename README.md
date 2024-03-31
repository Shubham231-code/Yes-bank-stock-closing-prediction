# Yes-bank-stock-closing-prediction
This Projet based on regression algorithms

This project aims to predict closing prices of stock using regression models. The following points explains the summary of this regression project.

Exploratory Data Analysis (EDA): In this step, the data was visualized and analysed to gain insights into the data. This step involved data cleaning and data pre-processing. The data was checked for missing values, duplicate records, and outliers. Data visualization techniques were used to identify patterns, trends, and relationships in the data.

Scrubing: After the EDA, the data was cleaned up by removing missing values, duplicates, and outliers. The data was standardized, and features were normalized.

Feature Engineering: In this step, new features were created from the existing data to improve the accuracy of the models. Features such as Year, Month, Quarter where created.

Pre-processing: In this step, the data was prepared for model implementation. The data was split into training and testing datasets. The training dataset was used to train the model, while the testing dataset was used to evaluate the performance of the model.

Model implementation: In this step, regression models were implemented to predict stock prices. Various regression models such as Linear Regression, Random Forest Regression, and Gradient Boosting Regression were trained on the dataset. The performance of each model was evaluated using metrics such as mean squared error (MSE), mean absolute error (MAE), and R-squared, also performed the cross-validation so that we can assess the performance of model when expose to unseen data. After considering all the indicator and matric we have chosen the Optimal_RandomForest model as final model to implement in production.

Model explainability: In this step, the models were analysed to understand the factors that influence the prediction of stock prices using the SHAP explain ability tool. The feature importance was analysed, and the models were interpreted to explain the relationship between the features and the predicted values.

Well-structured, formatted, and commented code is required.

Exception Handling, Production Grade Code & Deployment Ready Code will be a plus. Those students will be awarded some additional credits.

The additional credits will have advantages over other students during Star Student selection.

    [ Note: - Deployment Ready Code is defined as, the whole .ipynb notebook should be executable in one go
              without a single error logged. ]
Each and every logic should have proper comments.

You may add as many number of charts you want. Make Sure for each and every chart the following format should be answered.

# Chart visualization code
Why did you pick the specific chart?
What is/are the insight(s) found from the chart?
Will the gained insights help creating a positive business impact? Are there any insights that lead to negative growth? Justify with specific reason.
You have to create at least 15 logical & meaningful charts having important insights.
[ Hints : - Do the Vizualization in a structured way while following "UBM" Rule.

U - Univariate Analysis,

B - Bivariate Analysis (Numerical - Categorical, Numerical - Numerical, Categorical - Categorical)

M - Multivariate Analysis ]

You may add more ml algorithms for model creation. Make sure for each and every algorithm, the following format should be answered.
Explain the ML Model used and it's performance using Evaluation metric Score Chart.

Cross- Validation & Hyperparameter Tuning

Have you seen any improvement? Note down the improvement with updates Evaluation metric Score Chart.

Explain each evaluation metric's indication towards business and the business impact pf the ML model used.

Conclusion
The yes bank stock price dataset does not contain any null/missing value, also it's free form outliers.

While doing data visualization and cleaning we came to the following conclusion:

Some of the features are right-skewed so we have performed the log transformation.
The dependent variable having string linear correlation with all independent variables.
There is high-multicollinearity present in the data, so we introduce some new features.
There is sudden drop in the value of stock after 2018
We have seen the sudden increase in the price of stock in 2014 in a window of 10 months.
The VIFs values are extremely large, so we drop some features to reduce the VIFs scores.
We used the StandardScaler to scale our features.
In the hypothesis testing we mostly find the status quo, and one important conclusion is that the impact of COVID-19 is less as compared to the scam in 2020.

We have implemented the following regression models, so that we can assure that we get the best fit model.

Linear Regression
Ridge Regression
Lasso Regression
Polynomial Fit
Random Forest Regressor eXtreme Gradient Boosting (XGBoost) Regressor.
Upon implementing the given regression models, we came to the following important conclusions:

The Lasso performed better when compared to linear, ridge, polyfit. Polynomial fit performed bad in cross-validation as it shows the sign of overfitting.
The RandomForest and XGBoost are the final nominees for the model selection. as their overall performance in all matrices and in cross-validation are good compared to others. Finally we choose the RandomForest regressor, taking into consideration time-complexity and cross-validation score (mean CV = 95.77).
After model selection we used SHAP score to explain the model by using various plots, and came to know that OHL feature dominates the other feature as its correlation with DV is high and the second most important feature is Year.
At the end of the project we save our selected model in joblib and perform some sanity checks.
