# EDA-and-Logistic-regression
EDA and Logistic regression to predict whether a customer will churn


This code is performing exploratory data analysis (EDA) and logistic regression on a dataset of customer churn data in order to predict if a customer is likely to churn.

Importing libraries: The necessary libraries (pandas, matplotlib, seaborn, numpy, sklearn) are imported for use in the code.

Loading the data: The data is loaded into a Pandas DataFrame using the pd.read_csv function.

Cleaning the data: The code checks for missing values using the df.isnull().sum() method and finds that there are no missing values in the dataset.

Exploratory data analysis: Descriptive statistics for numerical columns are generated using the df.describe() method. The code then generates histograms and box plots for all numerical columns, and scatter plots for all pairs of variables. The code removes columns that contain string values in the Pandas DataFrame.

Preprocessing the data: The target feature "churn" is established as the "Exited" column of the dataframe. The code drops the target feature from the remaining features. The data is then scaled using the MinMaxScaler method from the sklearn library.

Splitting the data: The data is split into training and testing sets with a test size of 0.25 using the train_test_split method.

Logistic regression model: The logistic regression model is instantiated using the LogisticRegression method from the sklearn library. The model is fit to the training data using the logreg.fit method. Predictions are made for both the training and test sets using the logreg.predict method.

Model evaluation: Model performance is evaluated using various metrics such as accuracy score, precision score, recall score, F1 score, ROC curve, AUC, and confusion matrix. These metrics are calculated using the relevant methods from the sklearn library.

Model interpretation: The code calculates the residual differences between the actual training data and the predicted training data, and displays the number of times the model was correct or incorrect. The code also displays the normalized amount of times the model was correct. The decision function of the model is calculated for both the training and test sets, which can be used to calculate the false positive rate (fpr), true positive rate (tpr), and thresholds for each set.

The code concludes by presenting a summary of the logistic regression model's performance on the customer churn data.