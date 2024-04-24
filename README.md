# Customer-Churn-Prediction



### Introduction
The churn prediction project aims to develop a machine learning model to predict customer churn based on various features such as age, gender, annual income, tenure with the company, support calls, and monthly charges. This brief report summarizes the findings, methodology, and recommendations derived from the analysis.


### Findings
- The dataset consists of customer information including customerId, Age, Gender, financial details, and tenure with the company and also their churn status. 
- Exploratory data analysis (EDA) revealed a balanced distribution of features with no significant skewness.
- Customer churn, the target variable, appeared to be evenly distributed, indicating a balanced class.

![image](https://github.com/dineshgopalk98/Customer-Churn-Prediction/assets/93608867/7cbbb608-49c0-4c98-845d-3f095eedcd0a)
  
- There was no discernible pattern in churn rate based on customer tenure, suggesting that churn occurs across all tenure levels. The higest was with 7 years tenure and the lowest was with 5 years of tenure.  
- Correlation between features was generally low, with some exceptions such as the engineered feature 'money left' exhibiting a high positive correlation with annual income.

  ![image](https://github.com/dineshgopalk98/Customer-Churn-Prediction/assets/93608867/4e874862-b05b-4275-923e-198200629ab1)

- Statistical tests indicated no significant p-values, highlighting a lack of interdependence between features.
- Monthly charges emerged as the most influential feature in predicting churn

  ![image](https://github.com/dineshgopalk98/Customer-Churn-Prediction/assets/93608867/1a987184-ddb3-4e0c-9ec6-1cc37269e17f)

- The cumulative explained variance plot indicated that dimensionality reduction techniques may not yield meaningful results

  ![image](https://github.com/dineshgopalk98/Customer-Churn-Prediction/assets/93608867/bc927198-08e1-42a9-bac8-3dfce3f0acc6)

- The newly created feature ‘money_left’ did not have any significant impact on the dataset.
- Model evaluation using base classifiers showed modest accuracy scores, with SVM and Gaussian NB performing relatively better.
- Fine-tuning of models including SVM, Random Forest, and Logistic Regression did not significantly improve accuracy or ROC scores.
- Confusion matrices revealed challenges in predicting churn accurately, particularly due to non-correlatability between features.

  ![image](https://github.com/dineshgopalk98/Customer-Churn-Prediction/assets/93608867/4974c74a-45c7-4325-a7b5-26bdf1502a02)

### Methodology

#### Data Exploration
The initial step involved exploring the dataset to understand its structure and characteristics. This included analyzing features such as customer age, gender, annual income, tenure with the company, support calls, monthly charges, and churn status. Visualizations like histograms, bar plots, plotly plots and box plots were used to gain insights into feature distributions, class balance, and potential patterns.

#### Data Preprocessing
During preprocessing, the focus was on preparing the data for model training. This involved checking for outliers and ensuring data quality. There was no need to handle missing values as there were none in this dataset. Additionally, feature engineering was performed to create new variables like 'money left' to potentially enhance model performance.

#### Model Building
Multiple machine learning models were trained on the preprocessed dataset to predict churn. Algorithms such as Support Vector Machines (SVM), Gaussian Naive Bayes, Random Forest, XGBoost, Decision Tree Classifier, KNN, and Logistic Regression were utilized. This step aimed to establish baseline performances and identify promising candidates for further tuning.

#### Model Tuning
Fine-tuning was conducted on selected models to optimize their performance. Techniques such as hyperparameter tuning were employed to enhance model accuracy and generalization. Models were evaluated using metrics like accuracy, ROC-AUC score, and confusion matrices to assess their effectiveness. For this method, Support Vector Machines (SVM), Random Forest, and Logistic Regression  was used.

##### Interpretation
The interpretation phase involved analyzing the results obtained from the fine tuned models. This included examining feature importances, ROC curves, and confusion matrices to understand model behavior and performance. Insights were drawn regarding the influence of different features on churn prediction and the overall efficacy of the models.

### Recommendations
Based on the findings, the following recommendations are proposed to improve churn prediction:
- Incorporate additional features that provide more personalized insights into customer behavior, such as credit score, marital status, and location.
- Invest in feature engineering and data collection efforts to identify key indicators of churn and expand the dataset with relevant customer information.
- Collaborate with domain experts to guide the selection and creation of meaningful features that influence churn and other factors.
- Regularly monitor and update the model as new data becomes available to ensure its adaptability to changing customer dynamics.
- Utilize the model's output to identify customers at high risk of churn and develop targeted retention strategies, such as personalized offers, improved customer support, or loyalty programs, to proactively   
  address their needs and reduce churn rates.


### Conclusion
The customer churn prediction model, trained on a dataset with features including CustomerID, Age, Gender, Annual Income, Years with Company, Number of Support Calls, Monthly Charges, and Churn, achieved an accuracy of 52%. The well-balanced nature of the dataset eliminates the need for extensive preprocessing, allowing the focus to be on feature engineering and model development. However, the presence of a high correlation among features and the limited feature set highlights the challenges in building an effective churn prediction model. The lack of personalized customer information and meaningful features restricts the model's ability to capture the nuances of churn behavior.

Fine-tuning techniques, such as hyperparameter optimization and ensemble methods, did not significantly improve the model's accuracy and ROC scores. This suggests that the current feature set may not capture the full complexity of customer churn behavior. The current dataset provides a starting point, it's limitations emphasize the need for further analysis, incorporation of personalized customer attributes, and ongoing data exploration to enhance the model's predictive power and overall effectiveness.

By prioritizing the areas mentioned in recommendations and leveraging the insights gained from the churn prediction model, the company can take data-driven actions to improve customer retention. This will enable the proactive identification of at-risk customers and facilitate the implementation of effective strategies to enhance customer satisfaction, and revenue, and ultimately, reduce churn rates.

### Some useful visualizations(All the visualizations can be found in the notebook):
![image](https://github.com/dineshgopalk98/Customer-Churn-Prediction/assets/93608867/764872ed-5ced-4fed-aed8-e49f27f783c9)
![image](https://github.com/dineshgopalk98/Customer-Churn-Prediction/assets/93608867/c29ade36-8386-410c-b478-bb99a64a8bc0)
![image](https://github.com/dineshgopalk98/Customer-Churn-Prediction/assets/93608867/58949a03-5c78-44a6-85a8-45112c06bf70)
![image](https://github.com/dineshgopalk98/Customer-Churn-Prediction/assets/93608867/933b5035-87d6-4277-ab98-b8b9cf4c57db)




