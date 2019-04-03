## The Principle of Decision Tree
  1. The Definition of Decision Tree.
  2. Basis of Information Theory(Entropy, Joint Entropy, Condition Entropy, Information Grain and Gini Impurity)
  3. The Priciple of Regression Tree.
  4. The Solution of Overfitting in Decision Tree.
  5. The Evaluation of Model.
  6. The Illustration of Sklearn.
  
### 1. The Definition of Decision Tree.
Decision tree is a basic method of classification and regression. The classification decision tree model is a kind of 
tree knot that describes the classification of instances and it's made up of nodes and directed edges.

### 2. Basis of Information Theory(Entropy, Joint Entropy, Condition Entropy, Information Grain and Gini Impurity)
  * Entropy is a measure of uncertainty of a random variable. We assume that X is a discrete random variable with a finite
  number of values, and its probability distribution is
  Then the entropy of the random variable X is defined as
  
  * Joint Entropy. For a pair of discrete random variables subject to the joint distribution P(X,Y), the joint entropy H(X,Y) is
  defined as 
  
  * Condition Entropy is the uncertainty of the random variable Y under the given random variable X, the conditional entropy
  H(Y|X) of the random variable Y under the given random variable X. The conditional entropy H(Y|X) is defined as the mathematical expectation of the entropy of the conditional probability distribution of Y
  under the given X.
  
  In addition, when the probabilities in entropy and condition entropy are derived from the data estimate,especially the maximum likelihood
  estimate, the corresponding entropy and conditional entropy are called empirical entropy and empirical conditional entropy respectively.
  
  * Information gain represents the degree to which the information of feature X reduces the uncertainty of Y information. The 
  information gain g(D,A) of training data set D by feature A is defined as the difference between the empirical entropy H(D) of set D and
  the empirical conditional entropy H(D|A) of D given by feature A.
  g(D,A) = H(D) - H(D|A)
  Generally, the difference between entropy H(Y) and conditional entropy H(Y|X) is called mutual information.
  
  * Gini Index (Gini Inpurity). In classification problem, there are K classes, and the probability that the sample point belongs to the
  kth class is p_k, then the gini index of the probability distribution is defined as
  Gini(p) = 
  For binary classification problem, the gini index of the probability distribution is defined as
  For the given examples D, the gini index is defined as
  If features are divied into two parts D_1 and D_2 by feature A. Then under the condition of feature A, the gini index of set D is defined as
  
  ### 3. The Priciple of Regression Tree.
  The gini index is used to select the optimal feature and to determine the optimal binary segmentation point of the feature in classification tree.
  The steps of generating classification tree. Firstly,  calculate the gini indexs of all the features. Secondly,  choose the feature with the minimum gini
  index and the split point as the optimal variable and optimal point. We get two child nodes. Thirdly, the first and second steps are called
   recursively on the two child nodes until the stop condition is met. Finally we build a CART decision tree.
   
  ### 4. The Solution of Overfitting in Decision Tree.
  In CART decision tree, we use the pruning algorithm to avoid overfitting. For any given tree, the loss function is 
  C_α(T_t) = C(T)+α|T_t|
  The second part of the right-hand side |T_t| represents the number of leaf nodes, which represents the complixity of the model.
  The more nodes, the bigger the tree and the more complex the model. The hyper-parameter α is to balance the cost and complixity.
  
  In addition, there are many other ways to prevent overfitting such as ensemble algorithms, control the threshold of the gini impurith that meets the partition
  condition, control the number of leaf nodes and control the minimum number of leaf nodes in the next partition.
  
  ### 5. The Evaluation of Model.
 
  ### 6. The Illustration of Sklearn.
  
