## Machine Learning Approach to Credit Risk Scoring
- Objective: To predict the probability of default for a given customer
- Data: 
    - age: Age of the individual

    - ed: Education level (probably coded numerically)

    - employ: Years of employment

    - address: Years at current address

    - income: Annual income (possibly in $1,000s)

    - debtinc: Debt-to-Income ratio

    - creddebt: Credit card debt

    - othdebt: Other types of debt

    - default: Possibly a score or risk indicator for loan default

### Project Summary: Credit Default Prediction

- This project focuses on predicting whether an individual will **default on a loan** based on financial and demographic features such as age, income, employment history, debt-to-income ratio, etc.

- The dataset was preprocessed by:
  - Separating features and the target variable (`default`)
  - Splitting the data into **80% training and 20% testing**
  - Scaling the features using **StandardScaler** to improve model performance

- Three machine learning models were built and evaluated:
  1. **Random Forest Classifier** – Achieved an accuracy of approximately **82.1%**
  2. **Support Vector Machine (SVM)** – Tuned with `GridSearchCV`, also reached about **82.1% accuracy**
  3. **Logistic Regression** – Performed the best with an accuracy of **~83.6%**

- A **confusion matrix** was plotted to visualize the prediction results:
  - The models performed well in identifying **non-defaulters**
  - They were slightly less effective in identifying actual defaulters, indicating some **class imbalance** or sensitivity trade-off

- **Conclusion**: 
  - While all models performed well, **Logistic Regression** offered the best combination of **accuracy and interpretability**, making it a reliable choice for credit risk analysis.
