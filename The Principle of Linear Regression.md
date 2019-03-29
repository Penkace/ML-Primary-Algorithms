## The Principle of Linear Regression
  1. Introduction of Linear Regression
  2. The Advantages And Disadvantages of LR
  3. Loss Function, Cost Function And Objective Function
  4. Optimization Method(Gradient Descent, Newton Method And Quasi-Newton Method)
  5. The Evaluation of LR
  6. Illustration of Parameters in Sklearn
  
### 1. Introduction of Linear Regression
Linear Regression is simple and easy to build. As the basic model of machine learning, it highly descriptive and many nonlinear model with powful function can be derived from linear models by introducing hierarchical structure or high-dimensional mapping. The general form of linear regression is as follows.

### 2. The Advantages And Disadvantages of LR
  * Advantages: The comprehendsion and interpretation of LR are super intuitive, and regularization can avoid overfitting. In addition, the linear models is easy to update the data model by stochastic gradient descent.
  * Disadvantages: LR is bad at dealing with non-linear relationships, is not flexible enough at recognizing complex patterns. Especially, when adding the correct interaction terms or polynomials, LR is extremely tricky and time-consuming.
  
### 3. Loss Function, Cost Function And Objective Function
When I came into machine learning, I wasn't clear about the concept of these three functions. After reading some blogs, I can distinguish between these three functions.
  * Loss Function: Calculate the error of a example.
  * Cost Function: The mean of all the errors in the entire sample set.
  * Objective Function: The combination of cost function and regularization terms.
Actually, in the book statistical learning methods of LiHang, loss function and cost function have the same meaning and both of them are used to evaluate the degree of prediction error. There are several commomly used cost functions such as 0-1 loss function, quadratic loss function, absolute loss function and logarithmic loss function or loglikelihood loss function. The objective function in the book is called structural risk minimization. In the book machine learning by Zhou Zhihua, we always use mean square error to measure the performance of the model. The method based on military error minimization is called least square method, which is so useful that it has a wide range of applications. In addition, the evaluation metrics we commonly used are mean absolute error, mean squared error and root mean squared error.


### 4. Optimization Method(Gradient Descent, Newton Method And Quasi-Newton Method)
Gradient descent method is a common method to solve unconstrained optimization problems. The general form of GD is as follows.
Compared with gradient descent, Newton method and quasi Newton method has the characteristic of fast convergence. Each step of Newton method needs to solve the inverse matrix of the hayesian matrix of the objective function. It's complicated. Quasi Newton method simplifies the calculation process by approximating the inverse of the Hesse matrix by positive definite matrix.

### 5. The Evaluation of LR
The training error and the test error are the standard of evaluating learning algorithm. The evaluation indicators of model include error rate, accuracy, precision, recall and receiver operating characteristic. When ROC curve is not clear, we can calculate the **area under ROC curve** to compare the performance of two models.

### 6. Illustration of Parameters in Sklearn
The LR in sklearn has four parameters, two attributes and five methods.
* Four Parameters
  1. fit_intercept: default=True. There is a value b in LR which is intercept. This parameter specifies whether the intercept needs to be computed.
  2. normalize: dafault=False.This parameter is ignored when fit_intercept is set to False. If True, the regressors will be normalized before regression by subtracting the mean and dividing by the l2-norm.
  3. copy_X: default=True. If true, it will copy training data.
  4. n_jobs: default=None. Number of CPU specified when tasks are parallel. If the value is -1, all available CPUs are used.
* Two Attributes
  1. coef_: return estimated coefficients for the linear regression problem.
  2. intercept_: return the intercept mentioned above
* Five Methods
  1. fit: fit linear model. We need to deliver the training set and label.
  2. get_params: Get parameters for this estimator.
  3. predict: Predict other data using the linear model.
  4. score: return the coefficient of determination R^2 of the prediction.
  5. set_params: set the parameters of this estimator.
