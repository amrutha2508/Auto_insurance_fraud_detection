# Auto Insurance Fraud Detection
## Abstract :
nsurance fraud is one of the major issues that causes significant financial losses for both insurance company and public as well (high premium caused by loss to the companies). This project endeavors to create a machine learning model with the objective of classifying whether an insurance claim is fraudulent or not . The study employs techniques such as PCA for dimensionality reduction and over sampling for providing a balanced data set to the ML model. Different classifier Algorithms are used on this modified dataset and best model is chosen by comparing their ROC curves and recall rates.

## Data :
The data consists of 11565 instances and 1 target column ‘FraudFound_P’ and 33 attributes’ out of which 10 are numerical and 24 are categorical type.

## Data preprocessing :
1. Columns such as weekofmonth, dayofweek etc. are converted to categorical type .
2. Age distribution has values < 16 which is incorrect as per legal reasons , removal of these outliers is done.                .
3. The Data is highly imbalanced with only 0.059% of the records being fraud insurance cases. This problem is solved in further steps.
4. The minimum for claimsize if seen to be 0 which does not make sense, should remove this outlier. And the Claimsize value is large compared to the other columns log transformation was used to address the outliers in the data.         

## Feature Engineering : 
1. Convert the categorical variable are converted into binary type using One-Hot encoding technique resulting in 127 features.
2. Highly correlated features (with correlation greater than 0.,8) are identified and removed.
3. Since our only objective is to determine whether an insurance claim is fraudulent or not, we can use Principal Component Analysis to reduce the final number of features and the feature importance can be inferred based on the contributions of features to principal components and the variance explained by each component. .

## Methodology :
1. The imbalanced data problem was solved using an oversampling technique “SMOTE” .
2. Using PCA the no.of features for modeling were reduced from 127 to 7.
3. Different classification algorithms: Logistic Regression, Decision Tree, KNN, Random Forest, XGBoost, SVM are used. Grid Search technique is used to obtained best parameters for all the models.
4. The models performance were compared using the Confusion matrices, ROC curves , recall and F1- scores. 

