## Basic Conception of ML
  1. Supervised Learning
  2. Unsupervised Learning
  3. Generalization Ability
  4. Overfitting And Underfitting
  5. Variance And Bias
  6. Cross Validation
  7. Regularization
 
### 1. Supervised Learning
Supervised learning is the task of inferring a function from labeled training data. The training data consist of a set of training examples
In supervised learning, each instance has a pair consisting of an input object and a desired output value. What we do in supervised learning
is to analyze the training data and produce an infer function which can map new instances. It requires the learning algorithm to generalize
the training data to other situations in a "reasonable" way.

### 2. Unsupervised Learning
Unsupervised Learning is different from supervised learning. It tries to find the potential structure in unlabeled data. Therefore, there's no 
signal to evaluate a potential solution.

### 3. Generalization Ability
In machine learning, generalization ability refers to the generalization ability of the machine learning algorithm to the new sample.
The purpose of learning is to learn the rules hidden behind the train data. This rules can give appropriate output in another similar data.

### 4. Overfitting, Underfitting And Solution
Normally, we hope to get a classifier having a good performance on new data. We let our model to learn the universal rules from the training data in order to make a correct judgement in the new sample. Whereas, this will cause the model learns the potential rules of the training data which don't exist in other examples. As a result, the generalization ability of this model decreases. This is called 'Overfitting'. The most common way to solve overfitting is regularization.<br>
The opposite of overfitting is underfitting, which means the model don't well learn the general rules of training data. The reason of underfitting is the lack of features. So far as I know, there're two ways to overcome underfitting. One is to add polynomial and the other is to reduce parameter of the regularization.

### 5.Variance And Bias
Actually, we always want to know why the model has generalization ability and bias and variance is a tool to explain the generalization ability
of the learning algorithm. Bias measures the deviation degree between the exceptation prediction of the learning algorithm and the real result. It describes the
fitting ability of learning algorithm.<br>
Variance measures the change of learning performance caused by the change of trianing data with the same size and describes the influence
of data disturbance.

### 6. Cross Validation
Cross Validation is a common model selection methods. The data is divided into three parts and each part of the data distribution as consistent as possible. Then we use k-1 parts as training set and the rest is used as validation set. Finally we get k results and calculate the average amount. To a large extent, the stability and fidelity of the evaluation results by cross validation method depend on the value of k.

### 7. Regularization
Generally, regularization can avoid overfitting by controling the weight of parameters. The regularization we use in machine learning includes L1 regularization (it also called Lasso Regression) and L2 regularization (it also called Ridge Regression). L1 regularization is the sum of absolute values of each element of the weight vector. L2 regularization is the square root of sum of the squares of the weight vectors. The result of L1 regularization is that model is more sparse and has many parameters whose weights are equal to zero. It's considered that L1 regularization is the optimal convex approximation of L0 regularization and L1 regularization will throw away the useless features. L2 regularization tend to retain more features but their weight is closed to zero.
<img src="http://latex.codecogs.com/gif.latex?" />
<br>![](http://latex.codecogs.com/gif.latex?\\min_{f\subset F}\\frac{1}{N}\\sum_{i=1}^{N}L\\left(y_{i},f\\left(x_{i}\\right)\\right)+\\lambdaJ\\left(f\\right))
