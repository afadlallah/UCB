### Predicting Credit Card Fraud

**Ali Fadlallah**

#### Executive Summary

This project applies advanced machine learning techniques to predict fraudulent activities in credit card transactions. Using a dataset from the Kaggle platform featuring transactions from European cardholders [https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud), I employ several models including Logistic Regression, AdaBoost, Random Forest, XGBoost, LightGBM, and CatBoost to classify transactions as fraudulent or legitimate. The project aims to enhance fraud detection mechanisms, contributing to more secure credit card transactions.

#### Results

The project explored the effectiveness of various machine learning models to predict fraudulent transactions using a dataset from European cardholders. The models assessed include Logistic Regression, AdaBoost, Random Forest, XGBoost, LightGBM, and CatBoost. Each model was evaluated in both its base and optimized states.

The results indicate substantial differences in performance across the models and their configurations. Notably, all models achieved high accuracies, with several models reaching near-perfect training accuracies. However, the precision-recall area under the curve (PR AUC) and recall values vary significantly, which are critical in the context of fraud detection where the cost of false negatives is high.

The Random Forest and CatBoost models displayed exceptional performance in their optimized versions, achieving the highest PR AUC scores of 0.8931 and 0.8723, respectively. These models also showed excellent balance between precision and recall, suggesting they are well-suited for practical deployment in detecting fraudulent activities.

Conversely, the LightGBM model underperformed in its base configuration with the lowest PR AUC of 0.2606 and a significantly lower recall. However, its performance improved in the optimized version, reaching a PR AUC of 0.8699.

The fastest model in terms of training time was XGBoost, with its base version requiring only 0.8076 seconds. However, despite its speed, its precision and recall values were not the highest, which highlights a trade-off between training speed and detection effectiveness.

In summary, the optimized versions of the models generally outperformed their base counterparts, emphasizing the importance of model tuning in achieving high performance. The findings support the use of ensemble methods like Random Forest and CatBoost for fraud detection systems, which benefit from their ability to balance the need for quick processing with the necessity for high accuracy and recall.

#### Outline of Project

- Link to Notebook: [Initial Report and Exploratory Data Analysis (EDA)](https://github.com/afadlallah/UCB/blob/master/04%20Capstone%20Project%2020.1%20-%20Initial%20Report%20and%20Exploratory%20Data%20Analysis%20(EDA)/Capstone%20Project%2020.1%20-%20Initial%20Report%20and%20Exploratory%20Data%20Analysis%20(EDA).ipynb)

##### Contact and Further Information
For additional information or to discuss potential collaborations, please contact me on [LinkedIn](https://www.linkedin.com/in/ali-fadlallah/).