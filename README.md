# Credit Card Fraud Detection

![Credit Card Fraud Detection](https://st.depositphotos.com/1252160/4236/i/450/depositphotos_42366967-stock-photo-internet-theft-concept.jpg)

## Overview
Fraudulent activities in financial transactions pose significant challenges. Detecting and preventing fraud is crucial for maintaining trust and security in online transactions. This project leverages machine learning techniques, specifically the RandomForestClassifier algorithm, to develop a robust fraud detection system.

## Dataset
The dataset used for this project is sourced from [Kaggle](https://www.kaggle.com/datasets/kartik2112/fraud-detection). It contains various features related to credit card transactions.

## Data Preprocessing
- **Data Cleaning:** Null values are removed from both training and test datasets.
- **Feature Engineering:** Extracted hour, day, and month from `trans_date_trans_time` and dropped unnecessary columns.
- **Encoding:** Categorical variables like `merchant`, `category`, `gender`, `state`, `job`, and `city` are encoded using LabelEncoder.
- **Feature Scaling:** StandardScaler is applied to scale numeric features like `cc_num`, `amt`, `zip`, etc.

## Model Training and Evaluation
- **Splitting Data:** Data is split into training, validation, and test sets.
- **Random Forest Classifier:** Initially trained with default parameters and evaluated using classification metrics and ROC-AUC score.
- **Hyperparameter Tuning:** GridSearchCV is used to find the best parameters (`n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`) for improved performance.
- **Tuned Model Evaluation:** The model performance is evaluated on the validation set and further validated on the test set.

## Results
- **Validation Set Metrics:** Precision, Recall, F1-score, Confusion Matrix, and ROC-AUC score are reported.
- **Best Model:** The tuned RandomForestClassifier achieved improved performance on the validation and test sets.
- **Model Persistence:** The best model is saved using joblib for future use.

## Conclusion
This project demonstrates the application of machine learning in detecting credit card fraud. The RandomForestClassifier, optimized through hyperparameter tuning, offers a reliable solution for identifying fraudulent transactions.

Sure, here's a simple license statement that you can use for your project:

---

## License

MIT License

Copyright (c) 2024 [Sarvesh Mhatre](https://github.com/sarvesh-2109)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
