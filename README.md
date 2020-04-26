## Problem Statement
Dream Housing Finance company deals in all home loans. They have presence across all urban, semi urban and rural areas. Customer first apply for home loan after that company validates the customer eligibility for loan. Company wants to automate the loan eligibility process (real time) based on customer detail provided while filling online application form. These details are Gender, Marital Status, Education, Number of Dependents, Income, Loan Amount, Credit History and others. To automate this process, they have given a problem to identify the customers segments, those are eligible for loan amount so that they can specifically target these customers.

## The project is divided into below modules:
* Exploratory Data Analysis
* Data Preparation
* Predictive Modeling using different techniques.

## We will handle this problem in a structured way. We will be following the table of content given below.
* 1. Problem Statement
* 2. Loading Packages and Data
* 3. Understanding The Data
* 4. Univariate Analysis
* 5. Bivariate Analysis 
* 6. Missing Value Treatment
* 7. Outlier Treatment
* 8. Logistic Regression Without Feature Engineering
* 9. Logistic Regression With Stratified KFolds 
* 10. Feature Engineering
* 11. Logistic Regression With Feature Engineering
* 12. Decision Tree
* 13. Random Forest
* 14. XGBOOST
* 15. AdaBoost Classifier
* 16. Summary                    

## HYPOTHESIS GENERATED : 
Applicants with high income should have more chances of loan approval. Applicants who have repaid their previous debts should have higher chances of loan approval.Loan approval should also depend on the loan amount. If the loan amount is less, chances of loan approval should be high. Lesser the amount to be paid monthly to repay the loan, higher the chances of loan approval.

## UNIVARIATE ANALYSIS : 
* We will first look at the target variable, i.e., Loan_Status. As it is a categorical variable, look at its frequency table, percentage   distribution and bar plot.                                                     

* **Categorical features**: Gender| Married | Self_Employed | Credit_History | Loan_Status                      
* **Ordinal features**: Dependents | Education | Property_Area                                                                 
* **Numerical features**: ApplicantIncome | CoapplicantIncome | LoanAmount | Loan_Amount_Term                                          
                    
## BIVARIATE ANALYSIS : 
* After looking at every variable individually in univariate analysis, we will now explore them again                                     with respect to the target variable.                   
* First of all we will find the relation between target variable and categorical independent variables.                                   Let us look at the stacked bar plot now which will give us the proportion of approved and unapproved                                     loans.
* Now lets look at the correlation between all the numerical variables. We will use the heat map to                                       visualize the correlation. Heatmaps visualize data through variations in coloring. The variables                                         with darker color means their correlation is more.

 ## Missing value and outliers treatment
* After exploring all the variables in our data, we can now impute the missing values and treat the outliers because missing data and     outliers can have adverse effect on the model performance.
* We can consider these methods to fill the missing values:
   * For numerical variables: imputation using mean or median.
   * For categorical variables: imputation using mode.
                                           
## Model Building : Part I [Logistic Regression ]
Logistic regression is an estimation of Logit function. Logit function is simply a log of odds in favor of the event.This function creates a s-shaped curve with the probability estimate, which is very similar to the required step wise function.
 NOW : 
 1. train_test_split  
 2. LogisticRegression
 3. accuracy_score
 4. fit the logistic regression model.
                       
 ## Straified K-Fold cross validation
To check how robust our model is to unseen data, we can use Validation. It is a technique which involves reserving a particular sample of a dataset on which you do not train the model. Later, you test your model on this sample before finalizing it. Some of the common methods for validation are listed below:
  1. The validation set approach
  2. k-fold cross validation
  3. Leave one out cross validation (LOOCV)
  4. Stratified k-fold cross validation
                      
# Feature Engineering
* Based on the domain knowledge, we can come up with new features that might affect the target variable. We will create the following     three new features:
* **Total Income** 
  As discussed during bivariate analysis we will combine the Applicant Income and Coapplicant Income. If the total income is high,         chances of loan approval might also be high.
* **EMI** 
  EMI is the monthly amount to be paid by the applicant to repay the loan. Idea behind making this variable is that people who have high   EMI’s might find it difficult to pay back the loan. We can calculate the EMI by taking the ratio of loan amount with respect to loan     amount term.
* **Balance Income** 
  This is the income left after the EMI has been paid. Idea behind creating this variable is that if this value is high, the chances are   high that a person will repay the loan and hence increasing the chances of loan approval. 


## Model Building : Part II
* After creating new features, we can continue the model building process. So we will start with logistic regression model and then move   over to more complex models like RandomForest and XGBoost.
* We will build the following models in this section.
         1. Logistic Regression
         2. Decision Tree
         3. Random Forest
         4. XGBoost
         
## Summary 
We tried 5 different algorithms and the accuracy score achieved by each are as follow :

  1. Logistic Regression - 81%
  2. Decision Tree - 71%
  3. Random Forest - 81%
  4. XGBoost - 77%
  5. AdaBoost - 95.4%
      
