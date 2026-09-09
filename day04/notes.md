Here are clean Day 4 answers you can use as reference and then rewrite in your own words in notes.md.
1. Why are missing values a problem?
   Missing values can break some ML algorithms or reduce model quality because the model does not know what value should be used for that feature.
2. When would you use median instead of mean?
   Use the median when the numeric data has strong outliers or is highly skewed, because the median is less affected by extreme values.
3. What is mode?
   The mode is the value that appears most frequently in a column.
   Example:
   Delhi
   Hyderabad
   Delhi
   Mumbai
   Delhi
   Mode = Delhi.
4. Why do categorical variables need encoding?
   Most ML models work with numerical values, so text categories like Delhi, Mumbai, or Hyderabad need to be converted into numbers.
5. What does one-hot encoding do?
   It creates separate columns for each category and represents them using 0/1 or False/True.
   Example:
   city = Delhi
   
   city_Delhi      = 1
   city_Mumbai     = 0
   city_Hyderabad  = 0
6. Why do we scale features?
   Scaling puts numerical features on comparable ranges so that large-valued features do not dominate smaller-valued features in scale-sensitive models.
7. Which models usually benefit from scaling?
   Common examples are:
   - Logistic Regression
   - Linear Regression
   - KNN
   - SVM
   - Neural Networks
8. Do Random Forest and XGBoost usually require scaling?
   Usually, no. Tree-based algorithms split values based on thresholds, so feature magnitude generally does not affect them the same way.
9. Why do we fit the scaler only on training data?
   Because the test set should remain unseen. If we calculate scaling information using the test data, information from the test set leaks into training.
   Correct:
   scaler.fit(X_train)
   
   X_train_scaled = scaler.transform(X_train)
   X_test_scaled = scaler.transform(X_test)
   Or:
   X_train_scaled = scaler.fit_transform(X_train)
   X_test_scaled = scaler.transform(X_test)
10. What is data leakage?
    Data leakage happens when information that should not be available during training accidentally reaches the model.
    For example:
    Entire dataset
         ↓
    fit scaler
         ↓
    train/test split
    This is problematic because the scaler already learned statistics from the test data.
    Better:
    Dataset
       ↓
    Train/Test split
       ↓
    Fit preprocessing on TRAIN
       ↓
    Apply same preprocessing to TEST
The three Day 4 ideas I want you to remember most are:
Missing numeric value + strong outliers
→ Median

Categorical text
→ Encode it

Preprocessing that learns from data
→ Fit on training data only
And one especially important ML-engineering rule:
The test set should behave like future production data — the model should not learn anything from it beforehand.