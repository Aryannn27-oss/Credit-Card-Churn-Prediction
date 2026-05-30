# ChurnAnalytics

This project focuses on predicting credit card customer churn using machine learning. The objective is to identify customers who are likely to leave the bank and understand the factors that contribute to churn.

I used the BankChurners dataset containing over 10,000 customer records and built a complete machine learning pipeline starting from data cleaning and exploratory data analysis to model training, evaluation, and explainability.

## What I Did

* Performed exploratory data analysis (EDA) to understand customer behavior and churn patterns.
* Created several engineered features to capture customer engagement and transaction behavior.
* Trained and compared multiple machine learning models including Logistic Regression, XGBoost, and LightGBM.
* Evaluated models using ROC-AUC, PR-AUC, Precision, Recall, and F1 Score.
* Performed threshold tuning to find a better balance between precision and recall instead of relying on the default 0.5 threshold.
* Used SHAP (SHapley Additive Explanations) to understand both global feature importance and individual customer predictions.
* Saved the final model and preprocessing artifacts for future deployment.

## Results

Among all the models tested, XGBoost achieved the best performance:

* ROC-AUC: 0.992
* PR-AUC: 0.965
* Precision: 0.943
* Recall: 0.868
* F1 Score: 0.904

The model was able to correctly identify most churned customers while maintaining a low number of false positives.

## Key Insights

Some of the strongest indicators of churn were:

* Total transaction count
* Total transaction amount
* Transaction behavior changes over time
* Customer inactivity
* Revolving balance

The SHAP analysis showed that customers with low transaction activity and reduced engagement were significantly more likely to churn.

## Tools and Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* XGBoost
* LightGBM
* SHAP
* Joblib

## Files Included

* Data analysis notebook
* EDA visualizations
* Model comparison results
* SHAP explainability plots
* Confusion matrix
* Saved model files for deployment

## Future Improvements

The next step is to deploy the model using Streamlit so that customer information can be entered through a simple web interface and churn predictions can be generated in real time.

---

**Author:** Aryan Verma
B.Tech, IIT (BHU) Varanasi
