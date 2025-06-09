## Machine Learning Approach to Credit Risk Scoring

**Objective:** Predict the probability of loan default for a given customer using financial and demographic data.

**Dataset Features:**
- `age`: Age of the individual  
- `ed`: Education level  
- `employ`: Years of employment  
- `address`: Years at current address  
- `income`: Annual income  
- `debtinc`: Debt-to-Income ratio  
- `creddebt`: Credit card debt  
- `othdebt`: Other types of debt  
- `default`: Target variable (loan default indicator)

### 🔍 Project Summary

This project applies supervised machine learning techniques to classify whether a loan applicant is likely to default. The workflow included data preprocessing, feature scaling, model training, and evaluation.

### 📊 Exploratory Visualizations

#### 1. Income by Age
This plot shows how annual income varies with age. There’s a noticeable rise with age until ~50, followed by a drop.

![Income by Age](images/1.png)

#### 2. Debt-to-Income Ratio by Age
The debt-to-income ratio appears relatively stable but with spikes at older ages, potentially influencing default probability.

![Debt-to-Income by Age](images/2.png)

**Steps Taken:**
- Cleaned and split the dataset (80% training, 20% testing)
- Scaled features using `StandardScaler`
- Built and evaluated three models:
  1. **Random Forest Classifier** – ~82.1% accuracy
  2. **Support Vector Machine (SVM)** – Tuned with `GridSearchCV`, ~82.1% accuracy
  3. **Logistic Regression** – Best performance at ~83.6% accuracy

**Key Insights:**
- All models performed well in identifying non-defaulters.
- Slightly lower performance on predicting actual defaulters due to possible class imbalance.
- **Logistic Regression** was the most interpretable and accurate, making it a strong candidate for production use.


## Credit Scoring
- Methodology leveraged by Financial Institutions to determine the risk of non payment associated with loans 
- Why is it used? 
    - Credit Scoring enables decision making at all customer lifecycle stages
    - Removes the need to manually examine each loan customer
    - Clear understanding of Denial or Approval reasons leading to sound business approach
- How is it used?
    - Credit Scores are used to determine the following areas under Loan portfolios
        - Approval – Should the Loan be approved?
        - Pricing – What is the right Interest ?
        - Cross Sell – Can we sell another loan ?
        - Refinance – Should there be a change in Interest?
  
### 📉 Model Performance: Confusion Matrix

The confusion matrix below reflects predictions from the Logistic Regression model:

- Most correct predictions are in the top-left (non-defaulters correctly classified).
- Bottom-right is lighter, meaning some actual defaulters were missed.

![Confusion Matrix](images/3.png)
