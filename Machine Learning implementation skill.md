1. rmse (root mean square error) corresponds approximately to the std
2. Estimators predict a value based on the observed data
3. Using Sklearn fit() method to find the coefficient of all features in linear regression
4. Residual = Observed value - Predicted value   Residual plots are a good way to visualize the errors in the data in regression analysis
5. Pandas has a method of getting dummy variables to do with categorical variables
6. seaborn to visualize data such as sns.pairplot, sns.factorplot
7. to split training data set and testing data set, using train_test_split from sklearn.cross_validation
8. SVM do not directly provide probability estimates
9. If you have a large number of features which n is large, the number of training example is small, do not use kernel or equivalent to use what is called a linear kernel or a logistic regression
10. If the number of features is small and you have a pretty large training sample, you could use kernel.
11. Do perform feature scaling when using Gaussian kernel
12. If the number of features is small and the training set is intermediate, use SVM with a Gaussian kernel
13. If the number of features is small and the training set is large, use logistic regression or SVM without kernel
