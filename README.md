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
%matplotlib inline                     #sets the backend of matplotlib to the 'inline' backend: With this backend, the output                                         of plotting commands is displayed inline within frontends like the Jupyter notebook,                                         directly below the code cell that produced it. The resulting plots will then also be                                         stored in the notebook document
import warnings                        #To ignore any warnings 
warnings.filterwarnings("ignore")



# UNDERSTAND THE DATA : 

                      Data variables , Data types , Data shapes.

                    

# UNIVARIATE ANALYSIS : 
                        We will first look at the target variable, i.e., Loan_Status. As it is a categorical variable, let us                         look at its frequency table, percentage distribution and bar plot.                                                     
                        Now lets visualize each variable separately. Different types of variables are Categorical, ordinal                           and numerical.

                        Categorical features: These features have categories (Gender, Married, Self_Employed, Credit_History,                                                                                                                              
                                                                                                                 Loan_Status)
                        Ordinal features: Variables in categorical features having some order involved (Dependents,    
                                                                                                                   Education,                                                                                                                Property_Area)
                        Numerical features: These features have numerical values (ApplicantIncome, CoapplicantIncome,
                                                                                                                  LoanAmount,                                                                                                             Loan_Amount_Term)
                      
                      
                      
                      
                      
                      
                      
                   
