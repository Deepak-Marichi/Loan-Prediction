# Specifications

Python = 3.7
pandas = 0.20.3
seaborn = 1.0.0
sklearn = 0.19.1


# Loading Packages

import pandas as pd                    #Data
import numpy as np                     #For mathematical calculations 
import seaborn as sns                  #For data visualization 
import matplotlib.pyplot as plt        #For plotting graphs 
%matplotlib inline                     #sets the backend of matplotlib to the 'inline' backend: With this backend, the output                                                  of plotting commands is displayed inline within frontends like the Jupyter notebook,                                                    directly below the code cell that produced it. The resulting plots will then also be                                                    stored in the notebook document
import warnings                        #To ignore any warnings 
warnings.filterwarnings("ignore")



# UNDERSTAND THE DATA : 

                      Data variables , Data types , Data shapes.

                    

# UNIVARIATE ANALYSIS : 
                        We will first look at the target variable, i.e., Loan_Status. As it is a categorical variable, let us                                   look at its frequency table, percentage distribution and bar plot.                                                     
                        Now lets visualize each variable separately. Different types of variables are Categorical, ordinal                                       and numerical.

                        Categorical features: These features have categories (Gender, Married, Self_Employed, Credit_History,                                                                                                                              
                                                                                                                 Loan_Status)
                        Ordinal features: Variables in categorical features having some order involved (Dependents,Education,                                                                                                                Property_Area)
                        Numerical features: These features have numerical values (ApplicantIncome, CoapplicantIncome,                                                                                                          LoanAmount,Loan_Amount_Term)
                      
# HYPOTHESIS GENERATED : 

                        Applicants with high income should have more chances of loan approval.
                        
                        Applicants who have repaid their previous debts should have higher chances of loan approval.
                        
                        Loan approval should also depend on the loan amount. If the loan amount is less, chances of loan                                         approval should be high.
                        
                        Lesser the amount to be paid monthly to repay the loan, higher the chances of loan approval.        
                    
# BIVARIATE ANALYSIS : 
                        After looking at every variable individually in univariate analysis, we will now explore them again                                     with respect to the target variable.                   
                        Categorical Independent Variable vs Target Variable
                        First of all we will find the relation between target variable and categorical independent variables.                                   Let us look at the stacked bar plot now which will give us the proportion of approved and unapproved                                     loans.
                        Numerical Independent Variable vs Target Variable
                        Now lets look at the correlation between all the numerical variables. We will use the heat map to                                       visualize the correlation. Heatmaps visualize data through variations in coloring. The variables                                         with darker color means their correlation is more.
                 
 # Missing value and outliers treatment
                        After exploring all the variables in our data, we can now impute the missing values and treat the                                      outliers because missing data and outliers can have adverse effect on the model performance.
                        
                       We can consider these methods to fill the missing values:
                       For numerical variables: imputation using mean or median.
                       For categorical variables: imputation using mode.
                       
 # Making Dummy Variables
                       Now we will make dummy variables for the categorical variables. Dummy variable turns categorical                                        variables into a series of 0 and 1, making them lot easier to quantify and compare. 
                       
                       Let us understand the process of dummies first:
                       Consider the “Gender” variable. It has two classes, Male and Female.
                       As logistic regression takes only the numerical values as input, we have to change male and female                                      into numerical value.Once we apply dummies to this variable, it will convert the “Gender” variable                                      into two variables(Gender_Male and Gender_Female), one for each class, i.e. Male and Female.
                       Gender_Male will have a value of 0 if the gender is Female and a value of 1 if the gender is Male.
                       
  # Model Building : Part I [Logistic Regression ]
                       Logistic regression is an estimation of Logit function. Logit function is simply a log of odds in                                        favor of the event.This function creates a s-shaped curve with the probability estimate, which is very                                  similar to the required step wise function.
                       NOW : 
                       1. train_test_split  
                       2. LogisticRegression
                       3. accuracy_score
                       4. fit the logistic regression model.
                       
  # Straified K-Fold cross validation
                     To check how robust our model is to unseen data, we can use Validation. It is a technique which involves reserving                      a particular sample of a dataset on which you do not train the model. Later, you test your model on this sample                          before finalizing it. Some of the common methods for validation are listed below:
                      1. The validation set approach
                      2. k-fold cross validation
                      3. Leave one out cross validation (LOOCV)
                      4. Stratified k-fold cross validation
                      
# Feature Engineering
                  Based on the domain knowledge, we can come up with new features that might affect the target variable. We will create                  the following three new features:

# Total Income - 
As discussed during bivariate analysis we will combine the Applicant Income and Coapplicant Income. If the total income is high, chances of loan approval might also be high.
# EMI -
EMI is the monthly amount to be paid by the applicant to repay the loan. Idea behind making this variable is that people who have high EMI’s might find it difficult to pay back the loan. We can calculate the EMI by taking the ratio of loan amount with respect to loan amount term.
# Balance Income - 
This is the income left after the EMI has been paid. Idea behind creating this variable is that if this value is high, the chances are high that a person will repay the loan and hence increasing the chances of loan approval. 


# Model Building : Part II
After creating new features, we can continue the model building process. So we will start with logistic regression model and then move over to more complex models like RandomForest and XGBoost.

We will build the following models in this section.
         1. Logistic Regression
         2. Decision Tree
         3. Random Forest
         4. XGBoost
