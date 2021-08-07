# Credit_Risk_Analysis
Machine Learning models for credit risk analysis 

## Overview of Project
Jill commends you for all your hard work. Piece by piece, you’ve been building up your skills in data preparation, statistical reasoning, and machine learning. You are now ready to apply machine learning to solve a real-world challenge: credit card risk.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use `imbalanced-learn` and `scikit-learn` libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the `RandomOverSampler` and `SMOTE` algorithms, and undersample the data using the `ClusterCentroids` algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the `SMOTEENN` algorithm. Next, you’ll compare two new machine learning models that reduce bias, `BalancedRandomForestClassifier` and `EasyEnsembleClassifier`, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Deliverables: 
### 1. *Deliverable 1*: Use Resampling Models to predict credit risks 
### 2. *Deliverable 2*: Use the SMOTEENN Algorithm to predict credit risks 
### 3. *Deliverable 3*: Use Ensemble Classifier to predict credit risks 

## Resources: 
### 1. Data Source: `Module-17-Challenge-Resources.zip`and `LoanStats_2019Q1.csv`
### 2. Data Tools: `credit_risk_resampling_starter_code.ipynb` and `credit_risk_ensemble_starter_code.ipynb`
### 3. Software: `Python 3.9`, `Jupyter Notebook`and `Pandas`

## Analysis 
### Deliverable 1: Use Resampling Models to Predict Credit Risk 

    1. Using the information we’ve provided in the starter code, create your training and target variables by completing the following steps:
    - Create the training variables by converting the string values into numerical ones using the get_dummies() method.
   <img width="1089" alt="Screen Shot 2021-08-07 at 6 05 41 PM" src="https://user-images.githubusercontent.com/82353749/128614945-582e0946-2308-4f31-87e2-aeb66d6e42a0.png">

    - Create the target variables.
   <img width="1037" alt="Screen Shot 2021-08-07 at 6 07 02 PM" src="https://user-images.githubusercontent.com/82353749/128614971-a6811764-220d-4f70-9f3e-2d7efa036f57.png">

    - Check the balance of the target variables.
   <img width="1016" alt="Screen Shot 2021-08-07 at 6 08 30 PM" src="https://user-images.githubusercontent.com/82353749/128614982-d0f325c5-93c6-419d-8613-344e19c340a8.png">

    2. Next, begin resampling the training data. First, use the oversampling `RandomOverSampler`and `SMOTE` algorithms to resample the data, then use the undersampling `ClusterCentroids` algorithm to resample the data. For each resampling algorithm, do the following:
    - Use the `LogisticRegression` classifier to make predictions and evaluate the model’s performance.
    - Calculate the accuracy score of the model.
    - Generate a confusion matrix.
    - Print out the imbalanced classification report.
   
      (1) RandomOverSampler: 
   <img width="1019" alt="Screen Shot 2021-08-07 at 6 14 40 PM" src="https://user-images.githubusercontent.com/82353749/128615097-b69ba47e-bcf8-49fd-9b16-8eb49f44ff34.png">
   
      (2) SMOTE: 
   <img width="1010" alt="Screen Shot 2021-08-07 at 6 16 56 PM" src="https://user-images.githubusercontent.com/82353749/128615129-37d26b2e-78d4-4ea4-acdb-576f57e20066.png">
   
      (3) ClusterCentroids undersampling: 
   <img width="1007" alt="Screen Shot 2021-08-07 at 6 18 05 PM" src="https://user-images.githubusercontent.com/82353749/128615133-5b7d325d-8893-4042-a2a5-69da17c1a348.png">

### Deliverable 2: Use SMOTEENN algorithm to Predict Credit Risk
     1. Continue using your credit_risk_resampling.ipynb file where you have already created your training and target variables.
     2. Using the information we have provided in the starter code, resample the training data using the SMOTEENN algorithm.
     3. After the data is resampled, use the LogisticRegression classifier to make predictions and evaluate the model’s performance.
     4. Calculate the accuracy score of the model, generate a confusion matrix, and then print out the imbalanced classification report.

     
   <img width="998" alt="Screen Shot 2021-08-07 at 6 24 28 PM" src="https://user-images.githubusercontent.com/82353749/128615243-591b7831-0f38-4d15-b1aa-96e47bb8901b.png">

   <img width="1007" alt="Screen Shot 2021-08-07 at 6 20 06 PM" src="https://user-images.githubusercontent.com/82353749/128615270-da235b93-2dc9-41f5-a7fc-464685c85e8f.png">

### Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk

     1. Using the information we have provided in the starter code, create your training and target variables by completing the following:
       - Create the training variables by converting the string values into numerical ones using the get_dummies() method.
       - Create the target variables.
       - Check the balance of the target variables.
       
     2. Resample the training data using the BalancedRandomForestClassifier algorithm with 100 estimators.
   <img width="1014" alt="Screen Shot 2021-08-07 at 6 31 40 PM" src="https://user-images.githubusercontent.com/82353749/128615377-b3015b64-803e-450b-a4b5-257419e93712.png">
   
     3. After the data is resampled, use the LogisticRegression classifier to make predictions and evaluate the model’s performance.
     4. Calculate the accuracy score of the model, generate a confusion matrix, and then print out the imbalanced classification report.
   <img width="1154" alt="Screen Shot 2021-08-07 at 6 36 05 PM" src="https://user-images.githubusercontent.com/82353749/128615456-64f56b10-257e-47b9-986b-bd6b88de86eb.png">

     5. Print the feature importance sorted in descending order (from most to least important feature), along with the feature score.
   <img width="1034" alt="Screen Shot 2021-08-07 at 6 36 48 PM" src="https://user-images.githubusercontent.com/82353749/128615469-77be1421-9b0d-4c4f-b53d-c15a38abbb95.png">

     6. Next, resample the training data using the EasyEnsembleClassifier algorithm with 100 estimators.
   <img width="1018" alt="Screen Shot 2021-08-07 at 6 37 27 PM" src="https://user-images.githubusercontent.com/82353749/128615476-99b55e0e-0857-407a-b03b-115e67838f4b.png">

     7. After the data is resampled, use the LogisticRegression classifier to make predictions and evaluate the model’s performance. Calculate the accuracy score of the model, generate a confusion matrix, and then print out the imbalanced classification report.
   <img width="1024" alt="Screen Shot 2021-08-07 at 6 38 13 PM" src="https://user-images.githubusercontent.com/82353749/128615512-a23aff59-2c45-4618-8525-2624f2cbe30e.png">
   

## Summary 
For all models, `EasyEnsembleClassifier` rendered the most effective results. Provides a highest Score for all Risk loans. The precision is low or none for all the models. In General, above the 90% of the current analysis, utlizing `EasyEnsembleClassifier `will perform a High-Risk loan precision as a great value for the overall analysis.





    
