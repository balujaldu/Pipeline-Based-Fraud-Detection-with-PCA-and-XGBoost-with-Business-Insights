# Pipeline-Based-Fraud-Detection-with-PCA-and-XGBoost-with-Business-Insights
Developed a fraud detection system using the highly imbalanced Kaggle Fraud Detection dataset. Performed comprehensive data cleaning and preprocessing, applied PCA for dimensionality reduction, and implemented an XGBoost model within a pipeline. To handle class imbalance and improve generalization, utilized Stratified K-Fold Cross Validation.


This project focuses on detecting fraudulent financial transactions using Principal Component Analysis (PCA) and XGBoost within a machine learning pipeline. The dataset, sourced from Kaggle Fraud Detection, is highly imbalanced and simulates 30 days of real-world financial activity, with 744 time steps representing one-hour intervals. Each transaction is described by features such as transaction type, amount, customer IDs, account balances before and after the transaction, and fraud indicators (isFraud and isFlaggedFraud). Fraudulent activities primarily occur through unauthorized transfers and cash-outs, making early detection critical for financial security.

The data was first cleaned and preprocessed. Since there were no missing values, the focus was on removing irrelevant columns and eliminating outliers to ensure better feature distribution. The dataset was then split into training and testing sets for model evaluation. To reduce dimensionality and capture the most significant variance in the data, PCA was applied with 80% variance retained. XGBoost was chosen as the core classification model due to its ability to handle imbalanced data effectively. Using a pipeline, PCA and XGBoost were integrated, and hyperparameters were fine-tuned through GridSearchCV. The model was further validated using Stratified K-Fold Cross Validation with 5 folds to maintain class balance during training.

The optimized model, with PCA set at 0.80 and XGBoost configured with a tree depth of 10, achieved an impressive 96% test accuracy. Beyond achieving strong predictive performance, the project also focused on deriving meaningful business insights. PCA’s important features were analyzed to understand their relationship with fraudulent transactions. Visualizations were generated to highlight how fraud is influenced by transaction types, transaction amounts, and unusual balance patterns. Based on this analysis, practical recommendations were proposed, such as stricter monitoring of large transfers, flagging sudden balance changes, and applying tighter checks on high-value transactions exceeding 200,000 units.

Overall, this project not only demonstrates the effectiveness of combining dimensionality reduction with ensemble learning for fraud detection but also highlights how machine learning models can provide actionable insights for business decision-making and fraud prevention strategies.


dataset link:https://www.kaggle.com/datasets/sriharshaeedala/financial-fraud-detection-dataset


tech stack:
Python
Pandas, NumPy – Data cleaning & preprocessing
Scikit-learn – PCA, Pipeline, GridSearchCV, StratifiedKFold
XGBoost – Model training
Matplotlib, Seaborn – Visualization & business analysis.
