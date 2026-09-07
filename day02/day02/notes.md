1. Why do we split data into training and testing?
    We would basically split data into train and test because we want to check the accuracy of our model for unknown value because on know values we cannot trust the model
2. What is X_train?
    input values that goes into training
3. What is y_train?
    output values goes into training    
4. What is X_test?
    input values that goes into testing say 20%
5. What is y_test?
    output values that goes into testing say 20%
6. What does model.fit() do?
    model.fit use the x-train and y-train data to train the model and find patterns 
7. What does model.predict() do?
    the model which is trained will now predicts the output of the input values which are new or old aswell
8. Why don't we give y_test to the model?
If the answers are allready know to the model there is no use of spliting a y-test 
9. What does test_size=0.2 mean?
means 20% of data will go for testing
10. Why do we use random_state?
random state is used for selecting random value not in order or something we can use any random value say it 49 10 23 etc
Why use stratify=y?

To preserve the proportion of target classes
across training and testing datasets.