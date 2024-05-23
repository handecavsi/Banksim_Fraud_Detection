# BankSim Fraud Detection Project

This project focuses on detecting fraudulent transactions using the BankSim dataset. The dataset is preprocessed, visualized using Neo4j, and then analyzed with various machine learning models. The results are compared to identify the best performing model. This project includes detailed steps for data preprocessing, feature engineering, and model training.

**Table of Contents**
1. Project Overview
2. Data Preprocessing
3. Feature Engineering
4. Model Training
5. Graph Mining
6. Results
7. Conclusion

    
**1. Project Overview**
This project aims to detect fraudulent transactions in the BankSim dataset. The project involves the following steps:

- *Data Preprocessing:* Cleaning and preparing the data for analysis.
- *Feature Engineering:* Creating new features to improve model performance.
- *Model Training:* Training different machine learning models and evaluating their performance.
- *Graph Mining:* Visualizing and analyzing the data using Neo4j and graph mining algorithms.
- *Results Comparison:* Comparing the performance of different models and approaches.

**2. Data Preprocessing**
- Loading the Data
The BankSim dataset is loaded using Pandas. The initial steps involve checking for missing values and understanding the distribution of the target variable (fraud).

- Removing Unnecessary Columns
Columns such as step, customer, zipcodeOri, and zipMerchant are removed as they are either irrelevant or contain redundant information.

- Encoding Categorical Variables
Categorical variables like age, gender, category, and merchant are one-hot encoded to convert them into a format suitable for machine learning algorithms.

- Standardizing Features
The features are standardized using StandardScaler to ensure that all features contribute equally to the model.

- Dimensionality Reduction
Principal Component Analysis (PCA) is applied to reduce the dimensionality of the dataset while retaining 95% of the variance.

**3. Feature Engineering**
Additional features are created using graph mining algorithms in Neo4j. These features include:

- *merchDegree:* Degree of the merchant node.
- *custDegree:* Degree of the customer node.
- *custPageRank:* PageRank of the customer node.
- *merchPageRank:* PageRank of the merchant node.
- *merchCommunity:* Community detection for the merchant node.
- *custCommunity:* Community detection for the customer node.
These features are integrated back into the dataset for further analysis.

**4.Model Training**
*Machine Learning Models*
The following machine learning models are trained and evaluated:

- Random Forest Classifier
- Support Vector Machine (SVM)
- XGBoost Classifier

*Handling Class Imbalance*
SMOTE (Synthetic Minority Over-sampling Technique) is used to handle the class imbalance in the dataset.

*Cross-Validation*
Stratified K-Fold cross-validation is used to ensure robust evaluation of the models.

*Evaluation Metrics*
The models are evaluated using metrics such as accuracy, precision, recall, F1-score, and the classification report.

**5. Graph Mining**

- *Connecting to Neo4j*
The dataset is imported into Neo4j for graph visualization and analysis. The features are computed using Cypher queries and integrated back into the dataset.

- *Graph Features*
Graph mining algorithms such as PageRank and community detection are applied to extract meaningful features from the data.

**6. Results**

The performance of different models is compared based on their evaluation metrics. The results demonstrate the impact of graph-based features on model performance.

**7. Conclusion**

The project highlights the importance of data preprocessing, feature engineering, and graph mining in improving the performance of fraud detection models. The combination of machine learning and graph-based features provides a comprehensive approach to detecting fraudulent transactions.

*Prerequisites*

- Python 3.6 or higher
- Neo4j database
- Required Python libraries: numpy, pandas, py2neo, sklearn, xgboost, imblearn

*Reference*

- You can check out my article for more details:
- Detection of Fraud in Bank Payments Using Graph Mining and Machine Learning Algorithms [link](https://dergipark.org.tr/en/pub/dumf/issue/65099/1002110) 
  
