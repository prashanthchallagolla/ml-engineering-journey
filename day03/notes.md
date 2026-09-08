Classification: Your idea is right. Better definition: classification is when the model predicts a discrete category or label such as spam/not spam, cat/dog, or setosa/versicolor/virginica.

Regression: This one needs a small correction. It’s not “anything we cannot label.” Regression is specifically when the model predicts a continuous numerical value, such as salary, house price, temperature, or delivery time.

Why Iris is classification: ✅ Correct. 0, 1, and 2 are just encoded class labels. The numerical distance between them has no meaning.

Why salary is regression: ✅ Correct. Salary is a continuous numeric quantity.

Can classification have more than two classes? ✅ Yes. Two classes is binary classification; more than two is multiclass classification. Iris has three classes.

Why not accuracy_score for regression? ✅ Your reasoning is good. The stronger explanation is that regression predictions usually won’t exactly equal the actual value. If actual salary is ₹1,000,000 and predicted salary is ₹995,000, exact-match accuracy would call it completely wrong, even though it is close.

Why didn’t we use stratify=y for regression? You skipped this one. The answer is: regression targets are continuous values, not discrete classes, so there usually aren’t class proportions to preserve. stratify=y is mainly used in classification.

What does LinearRegression.fit() learn from? ✅ Directionally correct. More precisely: it learns the relationship between the input features in X_train and the continuous target values in y_train.

- Loan eligible / not eligible ✅
- Email spam / not spam ✅
- Image classification ✅
Regression:
- Rent or property value ✅
- Salary prediction ✅
- Forecasting ⚠️ — this depends on what you're forecasting. “Predict next month's sales amount” is regression. “Predict whether sales will increase or decrease” is classification.