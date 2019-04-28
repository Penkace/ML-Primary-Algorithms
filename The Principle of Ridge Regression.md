# The Principle of Ridge Regression
## What is the meaning of Ridge Regression
Ridge Regression, also known as Tikhonov regularization, is the regularization of Linear Regression. It adds a regularization term into the
loss function. This forces the learning algorithm not only to fit the data but also to keep the model weight as small as possible. Note that
the regularization term should only be added to the loss function during training. After training the model, you need to evaluate the performance
of the model using non-standard performance metrics.
It's common that the cost function used during training differs from the performance measure used for testing. In addition to normalization,
another reason they may differ
* * ridge regression (also known as Tikhonov regularization) * * is the regularization of the linear regression version: will be equal to
the $alpha Σ _ {I = 1} ^ n theta _i ^ 2 $regularization item added to the loss function.This forces the learning algorithm not only to fit
the data but also to keep the model weight as small as possible.Note that the ** regularization term should only be added to the loss
function ** during training.After training the model, you need to evaluate the performance of the model using non-standard performance
metrics.
It is common that the cost function used during training differs from the performance measure used for testing.In addition to 
normalization, another reason they may differ is that well-trained cost functions should have optimization-friendly derivatives, 
and performance measurements for testing should be as close to the end goal as possible.A good example is classifiers trained using 
cost functions, such as logarithmic losses (discussed later), but evaluated using precision/recall.
Super parameter controls the degree to which we want to normalize the model. 
* if $= 0$, then ridge regression is linear regression. 
* if $$is very large, the weight of ownership ends up very close to zero, resulting in a flat line through the mean of the data. 
Formula 4-8 shows the ridge regression cost function:
![image. PNG] (attachment: image. PNG)
