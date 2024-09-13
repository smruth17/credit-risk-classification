# Module 12 Report

## Overview of the Analysis


    The purpose of this analysis was to use various techniques to train and evaluate models on loan risk. The data came from a lending company that wanted help to identify the creditworthiness of borrowers. The data included columns for loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory hits, total debt and, loan status. The data was separated into two sections, features and labels. The label was loan status (X) and the features (y) were the remaining variables. Then the data was split into training and testing datasets. Finally, the logistic regression model was initiated and a classification report and confusion were generated. This was done to predict both the healthy loans (loan status of 0) and high risk loans (1). This was all completed in Jupyter Notebook - part 1.

    In Jupyter Notebook - part 2, I also ran the logistic regression model, but first looked at the dataset and determined that a standardscaler would be appropriate, since the standard deviation of a couple of the columns were high. Then we look at the value counts which showed a lot of imbalance and the correlation analysis in which we could have dropped columns (if we decided to do so). In addition to the logistic regression model (with the confusion matrix and classification report), I also looked at the Roc and Auc scores. I also looked at both the test data and train data metrics. Then I repeated the process using the Decision Tree, Random Forest, SVC, KNeighbors, Extra Trees, ADA boost, and Gradient Boost. Since part 2 data was scaled, I am going to show all of the results on part 2. 


## Results - Test Metrics

    -                           Precision      Recall      F1-Score      Accuracy      AUC                 ROC
    - Logistic Regression 0         1.00         1.00        1.00                
    - Logistic Regression  1         .87          .98         .92           .99         .99649277           1.00


    - Decision Tree 0                .99         1.00         .99       
    - Decision Tree 1                .87          .80         .83           .99         .93661555            .94


    - Random Forest 0               1.00         1.00         1.00  
    - Random Forest 1                .88          .87         .87           .99         .99588886           1.00


    - SVC 0                         1.00         1.00         1.00
    - SVC 1                          .87         1.00          .93          1.00        .99537706           1.00


    - KNeighbors 0                  1.00         1.00         1.00 
    - KNeighbors 1                   .87          .99          .93          1.00        .99602000           1.00


    - Extra Trees 0                  .99         1.00          .99
    - Extra Trees 1                  .87          .82          .85           .99        .96143576            .96


    - ADA Boost 0                   1.00         1.00         1.00 
    - ADA Boost 1                    .87          .99          .93          1.00        .99643059            1.00


    - Gradient Boost 0              1.00         1.00         1.00 
    - Gradient Boost 1               .87          .99          .93           .99        .99528499            1.00



## Summary
    Looking at all of the different machine learning models, they all seem to perform extremely well. All of the healthy loans (0) had perfect scores for precision, recall, and F1-score except for Decision Tree and Extra Trees. The high-risk loans (1) also had high scores for the aforementioned metrics all abover .82. The high-risk loans would be the most important to predict due to the implications that it has for the business. It is more critical to predict the high risk loans than the healthy ones.The accuracy of all models was either .99 or 1. The AUC scores are also extremely high. Overall, I would recommend using the KNeighbors model because it has the highest scores all around and is also the most explainable model. 


