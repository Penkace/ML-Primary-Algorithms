## The Principle of Logistic Regression
1. The Connection And Distinction Between Logistic Regression and Linear Regression
2. The Principle of Logistic Regression
3. The Derivation And Optimization of Loss Function of Logistic Regression
4. Regularization And Model Evaluation
5. The Advantages And Disadvantages of Logistic Regression
6. The Solution of Class-imbalance

### 1. The Connection And Distinction Between Logistic Regression and Linear Regression
[References](http://blog.sina.com.cn/s/blog_537ed51201019gu1.html)<br>
1. LR requires that variables follow normal distribution, while logistic regression doesn't require variable distribution.
2. LR requires that the independent variable is a continuous variable, while logistic regression requires the independent variable
is categorical variable.
3. LR requires a linear relationship between independent variables and dependent variables, while logistic regression doesn't.
4. Logistic regression is to analyze the relationship between the probability of taking a certain value of the dependent variable
and the independent variable, while linear regression is to directly analyze the relationship between the independent variale and 
the dependent variable.
Anyway, there're a lot of similarities between logistic regression and linear regression. The big difference is their dependent
variables. Both of them are belong to the same family, which we called generalized linear models.

### 2. The Principle of Logistic Regression 
![image](https://github.com/Penkace/ML-Primary-Algorithms/blob/master/1.png) 

### 3. The Derivation And Optimization of Loss Function of Logistic Regression
![image](https://github.com/Penkace/ML-Primary-Algorithms/blob/master/2.png) 
![image](https://github.com/Penkace/ML-Primary-Algorithms/blob/master/Logistic损失函数推导.jpg)
### 4. Regularization And Model Evaluation
The loss function of logistic regression can be solved by gradient descent method. It's similar to the derivation of the loss 
function for linear regression. The regularization of logistic regression is to add a regular term into the loss function.
as the hyperparameter, alpha adjust the punishment.
<br>The model evaluations we use include accuracy, recall, precision, ROC and AUC. 

### 5. The Advantages And Disadvantages of Logistic Regression
The advantages of logistic regression:
  1. It's easy to understand and implement and we can know probabilities of examples.
  2. Thanks to the sigmoid function, it's robust to the noisy in data.
  3. The speed of training is fast.
  4. The results are not affected by multicollinearity.
The disadvantages of logistic regression:
  1. Easy to underfitting.
  2. It's inefficiency when the feature space is large.
  3. When the probability is closed to zero, it will shock and the threshold cannot be determined.
  
### 6. The Solution of Class-imbalance
This problem is normal for logistic regression. In the book 'Machine Learn', the strategy of class-imbalance.
1. Undersampling. Removing some counterexamples makes the number of positive and negative examples close.
2. Oversampling. Adding some positive examples makes the number of positive and negative examples close.
3. Threshold-moving. 
