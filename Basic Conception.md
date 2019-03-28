## Basic Conception of ML
  1. Supervised Learning
  2. Unsupervised Learning
  3. Generalization Ability
  4. Overfitting And Underfitting
  5. Variance And Bias
  6. Cross Validation
 
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

### 4. Overfitting And Underfitting
Normally, we hope to get a classifier having a good performance on new data. We let our model to learn the universal rules from the training data
in order to make a correct judgement in the new sample. Whereas, this will cause the model learns the potential rules of the training data which don't exist
in other examples. As a result, the generalization ability of this model decreases. This is called 'Overfitting'.<br>
The opposite of overfitting is underfitting, which means the model don't well learn the general rules of training data.

### 5.Variance And Bias
Actually, we always want to know why the model has generalization ability and bias and variance is a tool to explain the generalization ability
of the learning algorithm. Bias measures the deviation degree between the exceptation prediction of the learning algorithm and the real result. It describes the
fitting ability of learning algorithm.<br>
Variance measures the change of learning performance caused by the change of trianing data with the same size and describes the influence
of data disturbance.

### 6. Cross Validation
