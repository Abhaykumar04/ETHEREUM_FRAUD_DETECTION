




## Ethereum Fraud Detection
![image](https://github.com/Abhaykumar04/ETHEREUM_FRAUD_DETECTION/assets/112232080/28de94c6-42dd-4ef3-bf3e-c3748892f2c3)


This project focuses on detecting fraud in Ethereum transactions using machine learning techniques. Ethereum is a decentralized blockchain platform that allows the creation and execution of smart contracts. With the increasing adoption of cryptocurrencies and blockchain technology, detecting fraudulent transactions has become crucial for maintaining the integrity and security of the Ethereum network.

### Dataset

The project utilizes a dataset consisting of Ethereum transactions, including various features such as transaction amount, timestamp, sender address, recipient address, gas price, and more. The dataset provides a labeled set of transactions, with each transaction marked as either fraudulent or legitimate.

### Data Preprocessing

Before building the fraud detection models, the dataset undergoes preprocessing steps to prepare the data for analysis. The following preprocessing techniques are applied:

- Data Cleaning: Handling missing values, removing duplicates, and handling outliers, if applicable.
- Feature Engineering: Creating new features from the existing data to capture additional information or patterns.
- Data Transformation: Applying transformations to the data, such as power transformations using the `PowerTransformer` from scikit-learn, to improve model performance.
- Handling Class Imbalance: Since fraud transactions are relatively rare compared to legitimate transactions, addressing class imbalance is important. The `SMOTE` algorithm from the imbalanced-learn package is used to oversample the minority class (fraudulent transactions) and balance the dataset.

### Model Development

Several machine learning models are trained to detect fraudulent Ethereum transactions. The following models are implemented:

- Logistic Regression: A linear classification model that estimates the probability of a transaction being fraudulent.
- Random Forest Classifier: An ensemble model consisting of multiple decision trees to classify transactions.
- XGBoost: A gradient boosting framework that combines weak learners (decision trees) into a strong predictive model.

To find the best combination of hyperparameters for each model, a grid search is performed using the `GridSearchCV` class from scikit-learn. The grid search explores various combinations of hyperparameters and evaluates their performance using cross-validation.

### Model Evaluation

The trained models are evaluated using various performance metrics to assess their effectiveness in detecting fraudulent transactions. The following evaluation metrics are calculated:

- Confusion Matrix: A matrix showing the true positive, true negative, false positive, and false negative predictions of the models.
- ROC AUC Score: The area under the Receiver Operating Characteristic (ROC) curve, which measures the model's ability to distinguish between fraudulent and legitimate transactions.
- ROC Curve: A graphical representation of the true positive rate (sensitivity) against the false positive rate (1 - specificity) at various classification thresholds.
- Classification Report: A summary of various metrics such as precision, recall, and F1-score for both fraudulent and legitimate transactions.

These evaluation metrics provide insights into the models' performance and help in selecting the best model for fraud detection.

### Model Deployment and Serialization

Once the best-performing model is identified, it can be deployed to detect fraudulent Ethereum transactions in real-time. The model can be serialized using the `pickle` module, which allows the model object to be saved as a file and loaded later for predictions without retraining.

The serialized model can then be integrated into an application or system that monitors Ethereum transactions, providing a reliable fraud detection mechanism to safeguard the Ethereum network.

Please refer to the code files in this repository for a detailed implementation of the Ethereum fraud detection project, including data preprocessing, model training, evaluation, and deployment.

Feel free to customize and modify the code according to your specific requirements and data.
