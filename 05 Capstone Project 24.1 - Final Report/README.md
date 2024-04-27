### Predicting Credit Card Fraud

**Ali Fadlallah**

#### Executive Summary

This project applies advanced machine learning techniques to predict fraudulent activities in credit card transactions. Using a dataset from the Kaggle platform featuring transactions from European cardholders [https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud), I employ several models including Logistic Regression, AdaBoost, Random Forest, XGBoost, LightGBM, and CatBoost to classify transactions as fraudulent or legitimate. The project aims to enhance fraud detection mechanisms, contributing to more secure credit card transactions.

#### Rationale

Financial losses from credit card fraud are significant and growing, impacting consumers and financial institutions globally. Efficient and accurate fraud detection systems are essential to reduce losses and maintain trust in financial systems. This project seeks to leverage machine learning to improve fraud detection rates, thereby reducing the incidence of fraud and its associated costs.

#### Research Question

Can the application of Logistic Regression and other machine learning models on transactional data significantly improve the detection of fraudulent credit card transactions?

#### Data Sources

The dataset, "Credit Card Fraud Detection," comes from Kaggle and features 284,807 transactions made by European cardholders in September 2013. Each transaction includes 30 features derived from PCA, alongside the transaction amount and a timestamp, with a target variable indicating whether the transaction was fraudulent.

Link: [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

#### Methodology

- **Initial Data Exploration**: Performed initial exploration of the dataset and its features.
- **Data Preprocessing**: Data was checked for missing values and distributions. Although there existed a significant class imbalance, the dataset was not balanced for this project.
- **Exploratory Data Analysis (EDA)**: Analyzed transaction amounts and time to understand patterns in fraudulent activities. Utilized correlation matrices to examine relationships between features.
- **Model Building**: Trained base models (Logistic Regression, AdaBoost, Random Forest, XGBoost, LightGBM, CatBoost) and tuned hyperparameters to optimize performance.
- **Evaluation**: Used metrics like accuracy, precision, recall, F1-score, and AUC-PR curve to evaluate model performance.

#### Results

The project explored the effectiveness of various machine learning models to predict fraudulent transactions using a dataset from European cardholders. The models assessed include Logistic Regression, AdaBoost, Random Forest, XGBoost, LightGBM, and CatBoost. Each model was evaluated in both its base and optimized states.

The results indicate substantial differences in performance across the models and their configurations. Notably, all models achieved high accuracies, with several models reaching near-perfect training accuracies. However, the precision-recall area under the curve (PR AUC) and recall values vary significantly, which are critical in the context of fraud detection where the cost of false negatives is high.

The Random Forest and CatBoost models displayed exceptional performance in their optimized versions, achieving the highest PR AUC scores of 0.8931 and 0.8723, respectively. These models also showed excellent balance between precision and recall, suggesting they are well-suited for practical deployment in detecting fraudulent activities.

Conversely, the LightGBM model underperformed in its base configuration with the lowest PR AUC of 0.2606 and a significantly lower recall. However, its performance improved in the optimized version, reaching a PR AUC of 0.8699.

The fastest model in terms of training time was XGBoost, with its base version requiring only 0.8076 seconds. However, despite its speed, its precision and recall values were not the highest, which highlights a trade-off between training speed and detection effectiveness.

In summary, the optimized versions of the models generally outperformed their base counterparts, emphasizing the importance of model tuning in achieving high performance. The findings support the use of ensemble methods like Random Forest and CatBoost for fraud detection systems, which benefit from their ability to balance the need for quick processing with the necessity for high accuracy and recall.

#### Next Steps

- **Model Improvement**: Further tuning of model parameters and integration of ensemble methods.
- **Feature Engineering**: Investigation into new features that could improve model sensitivity to fraudulent transactions.
- **Real-Time Implementation**: Explore deployment strategies for implementing these models in real-time transaction processing systems.
- **Global Scaling**: Test the adaptability of models across different demographics and transaction environments.

#### Outline of Project

- Link to Notebook: [Final Report](https://github.com/afadlallah/UCB/blob/master/05%20Capstone%20Project%2024.1%20-%20Final%20Report/Capstone%20Project%2024.1%20-%20Final%20Report.ipynb)

##### Contact and Further Information
For additional information or to discuss potential collaborations, please contact me on [LinkedIn](https://www.linkedin.com/in/ali-fadlallah/).