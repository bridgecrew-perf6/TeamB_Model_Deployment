# TeamB_Model_Deployment
Predicting Mortgage Backed Securities Prepayment Risk Using Machine Learning

![1200px-Freddie_Mac svg](https://user-images.githubusercontent.com/78646864/136017729-8b90fe01-9fdc-4840-8887-b271c266e51c.png)



## Introduction
Mortgage-backed securities, called MBS, are bonds secured by home and other real estate loans. They are created when a number of these loans, usually with similar characteristics, are pooled together. As the borrowers gradually pay off the underlying mortgage loans, the investors receive payments of interest and principal. A large risk factor in MBS lies in the possibility of prepayments. Prepayments are payment by borrowers,who pay back a part, or the full amount of the loan earlier than discussed in their mortgage contract. The aim of our project is to develop various Machine Learning models that could predict the prepayment risk of mortgage loans by using machine learning techniques like Random Forest, Logistic Regression and Support Vector Machine (SVM) algorithms.

## Dataset
We use Freddie Mac’s home loans dataset. This dataset contains 291452 rows which represent the number of mortgages/ data points and 28 columns representing different features of the data.

## Important Features

*CIBIL Score:* - A three digit number summarizing the borrower’s creditworthiness, which may be indicative of the likelihood that the borrower will timely repay future obligations. Generally, the CIBIL score disclosed is the score known at the time of acquisition and is the score used to originate the mortgage.

*MORTGAGE INSURANCE PERCENTAGE (MIP):* The percentage of loss coverage on the loan, at the time of Freddie Mac’s purchase of the mortgage loan that a mortgage insurer is providing to cover losses incurred as a result of a default on the loan.

*ORIGINAL COMBINED LOAN-TO-VALUE (OCLTV):* In the case of a purchase mortgage loan, the ratio is obtained by dividing the original mortgage loan amount on the note date plus any secondary mortgage loan amount disclosed by the Seller by the lesser of the mortgaged property’s appraised value on the note date or its purchase price.

*DEBT-TO-INCOME (DTI) RATIO:* Disclosure of the debt to income ratio is based on (1) the sum of the borrower's monthly debt payments, including monthly housing expenses that incorporate the mortgage payment the borrower is making at the time of the delivery of the mortgage loan to Freddie Mac, divided by (2) the total monthly income used to underwrite the loan as of the date of the origination of the such loan.

*LOAN-TO-VALUE (LTV):* In the case of a purchase mortgage loan, the ratio obtained by dividing the original mortgage loan amount on the note date by the lesser of the mortgaged property’s appraised value on the note date or its purchase price.

*PREPAYMENT PENALTY MORTGAGE (PPM):* - Denotes whether the mortgage is a PPM. A PPM is a mortgage with respect to which the borrower is, or at any time has been, obligated to pay a penalty in the event of certain repayments of principal.

*ORIGINAL LOAN TERM:* A calculation of the number of scheduled monthly payments of the mortgage based on the First Payment Date and Maturity Date.

*NUMBER OF BORROWERS:* The number of Borrower(s) who are obligated to repay the mortgage note secured by the mortgaged property.

#### Target Variable
Our Target variable is EverDelinquent. It equals 0 if the borrower paid the loan on time. It equals 1 if the borrower did not pay the loan for more than 30 days at any time in the duration of loan repayment.

## Model Used:
This is a Classification problem so we use Random Forest Classifier and Linear Support Vector Classifier for Model Building.
### Training and Testing dataset
Split dataset into 80 % for Training and 20% for testing

#### We achieve 100% accuracy in both the models which indicates data leakage. This is due to sub duplicates in the dataset which cannot be solved unless we change the entire dataset.


**STEPS for web app development:**

**1.** Importing required Libraries and intialize the flask object.

**2.** Load pickle file for pipelined random forest model

**3.** We have created our web page using **HTML** and styling of web page using **CSS**.

**4.** Now , we have to join our HTML and CSS page with web app using Flask **app.route('/')**.

**5.** Now we take all the Inputs.

**6.** After getting all the inputs finally predict the output using **app.route('/predict')**.

## Requirement:

![image](https://user-images.githubusercontent.com/56593219/175295481-76829f59-9ccd-477c-921c-4d4a1f4072c9.png)

to run the file:

pip install -r requirements

change the current working directory to where the files are present.

flask run

Deployment link: https://prepayment-prediction.herokuapp.com/

## Deploy Our Model Using Heroku Platform:

**User Interface**

![image](https://user-images.githubusercontent.com/56593219/175866157-45ec0e89-d398-47ca-a48f-634e6f59403b.png)


**Future Scope:**

We can try to find the sub duplicates to solve the problem of data leakage. Neural networks can be used to get knowledge on working with arrays.


**Output:**

![image](https://user-images.githubusercontent.com/56593219/175866306-da24518c-8a96-4c90-bb80-aafab55c7532.png)


**Conclusion:**

Above the output predicted by our model is **There is a risk of prepayment** .
if there is a prepayment risk for the loan then the model predicts **No risk of prepayment**.

We utilized 21 parameters from Freddie Mac’s Home Loan dataset as an input to predict whether an individual will prepay their mortgage loan or not. We have employed Random Forest Classifier and Linear Support vector Classifier Algorithm to predict the results. We have used almost 90% of data from the source file and performed various techniques of data cleaning to make it suitable for modeling. We applied train-test split and combination of various encoding and scaling techniques on the data to enhance the performance of our model. Our project explores number of machine learning techniques, and both of our model performed very well overall and eclipsed the 100% accuracy mark.

Prepayment risk prediction is quite helpful to the loan providers although there is already a big part of information stored in CIBIL score.

**Browse link:**

App link - https://prepayment-prediction.herokuapp.com/


Link to github code using django: https://github.com/amrahmed-swe/prepayment-predicition-deploy-django
