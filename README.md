# MSCS 634 – Advanced Big Data and Data Mining  
## Project Deliverable 2 – Regression Modeling and Performance Evaluation  

**Dataset:** Online_Retail_II  
**Notebook:** Deliverable2.ipynb  
**Group Members:**  
Pabitra Bhandari  
Haeri Kyoung  
Vamsi Krishna Gajulapalli  
Prakash Tamang

---

# 1. Deliverable Objective

The purpose of Deliverable 2 is to develop regression models to predict a selected outcome variable using structured feature engineering and systematic model evaluation techniques. This phase emphasizes model construction, performance comparison, and generalization through cross-validation.

---

# 2. Dataset Summary

The Online Retail II dataset contains transactional records from a UK-based online retailer. The dataset includes:

- Invoice
- StockCode
- Description
- Quantity
- InvoiceDate
- UnitPrice
- Customer ID
- Country

The dataset satisfies project requirements:

- More than 500 records
- Minimum of 8-10 attributes
- Combination of numerical and categorical features

For regression modeling, numerical and engineered features were selected to predict transaction-level outcomes.

---

# 3. Feature Engineering

Feature engineering was performed to enhance predictive performance and improve model stability.

Key steps included:

- Removal of canceled or invalid transactions
- Creation of a derived feature: **Total Transaction Value (Quantity × UnitPrice)**
- Extraction of date components from InvoiceDate where relevant
- Encoding of categorical variables where necessary
- Selection of relevant predictor variables based on correlation analysis
- Optional scaling of numerical features to improve model convergence

These transformations improved signal strength and reduced unnecessary noise.

---

# 4. Regression Models Developed

At least two regression models were implemented:

### Model 1: Linear Regression
- Used as a baseline model
- Provides interpretability of feature relationships

### Model 2: Regularized Regression (Ridge or Lasso)
- Applied to reduce overfitting
- Controls coefficient magnitude
- Improves generalization performance

Both models were trained using structured train-test splitting.

---

# 5. Model Evaluation

Models were evaluated using the following metrics:

- R-squared (R²)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

These metrics were displayed clearly within the notebook to allow direct comparison between models.

---

# 6. Cross-Validation

To assess generalization ability:

- K-fold cross-validation was applied.
- Performance metrics were averaged across folds.
- Variability between folds was analyzed.

Cross-validation ensured that the model performance was not dependent on a single data split.

---

# 7. Model Comparison and Results

The regression models were compared using R², MSE, and RMSE.

Key observations:

- The regularized model demonstrated improved stability across folds.
- Linear Regression performed well but was more sensitive to outliers.
- Feature engineering significantly improved predictive accuracy.
- Cross-validation confirmed consistent model behavior.

The best-performing model was selected based on lower RMSE and higher R² values.

---

# 8. Meaningful Insights

From the regression analysis:

- Quantity and UnitPrice strongly influence total transaction value.
- Outliers significantly impact prediction error.
- Regularization reduces overfitting and improves reliability.
- Derived features improve predictive power.

These insights validate the importance of feature engineering in supervised learning tasks.

---

# 9. Challenges and Solutions

### Challenge 1: Outliers in Retail Data
Retail transactions contain extreme values.  
Solution: Applied filtering and regularization to stabilize model behavior.

### Challenge 2: Overfitting Risk
Initial models showed variance between training and testing results.  
Solution: Implemented Ridge/Lasso regression and cross-validation.

### Challenge 3: Feature Selection
Too many features increased complexity.  
Solution: Used correlation analysis and domain logic to select relevant predictors.

### Challenge 4: Data Preparation Consistency
Date parsing and categorical encoding required careful handling.  
Solution: Explicit preprocessing steps were documented and applied systematically.

---

# Conclusion

Deliverable 2 successfully implements regression modeling using structured preprocessing, feature engineering, performance evaluation, and cross-validation. The results demonstrate that properly engineered features and regularization techniques improve predictive stability and generalization.

This deliverable provides a strong foundation for subsequent tasks in classification, clustering, and pattern mining (Deliverable 3).

