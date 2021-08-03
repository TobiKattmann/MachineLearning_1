# MC_SS20_3.PNG

a) Q: Random forests are a machine learning model in which . . .
1. a decision tree is trained for each label and a data point is labeled by all the trees.
2. a forest is trained and during evaluation a random walk through this forest is gene-
rated and its path nodes are used as the label.
3. multiple decision trees are trained, which vote during evaluation.

A:
3. Multiple decision trees are trained, which vote during evaluation.

The other two don't really make sense.

b) Q:K-means is . . .
1. an unsupervised algorithm for feature extraction.
2. an unsupervised algorithm for determining clusters.
3. a supervised algorithm which evaluates a label by taking the mean of k ML models

A: 2. an unsupervised algorithm for determining clusters.

In the 1st answer. PCA e.g. is used for feature extraction [link](https://towardsdatascience.com/feature-extraction-techniques-d619b56e31be)

In the 3rd answer one could write the following to make it correct for random forests: an unsupervised algorithm which evaluates a label by taking the mean of "k" decision trees. 


c) Q: The non-linearity of neural networks originates from . . .
1. the stacking of multiple layers.
2. its activation function.
3. its use of kernels.

A: 2. its activation function. [link](https://stats.stackexchange.com/questions/222639/what-makes-neural-networks-a-nonlinear-classification-model)

For the 3rd answer: We did not speak about kernels used for NN.

For the 1st answer: If the activation function were to be identiy, then one layer evaluation would be a matrix(weights) vector(inputs) multiplication. 


d) Q: In neural networks the choice of activation function is usually . . .
1. not limited by any factor.
2. limited to differentiable functions.
3. limited to functions which are differentiable almost everywhere.

A: 3. limited to functions which are differentiable almost everywhere.

The 2nd is definitly wrong, e.g. ReLU which is not differentiable in 0.

The 1st is wrong. Think about a function that is nowhere differentiable (e.g. Weierstrass function).
Then it would be impossible to compute a gradient for NN training.

e) Q: Least squares regression . . .
1. can be trained by gradient descent.
2. is an algorithm which tries to find a minimum square which encapsulates all data
points.
3. cannot evaluate the label of a data point with O(d) computations

A: 1. can be trained by gradient descent.

Note: In the lecture we computed the analytical solution for RR. But for plain Regression the analytical solution is `w=(X X^T)^-1 X y`

The 2nd is wrong: LSR is an algorithm that tries to find an affine linear function that reduces the least squares error to the original data.

The 3rd is wrong: In order to evaluate the label(i.e. the value) of a new data point the linear function `w^t x + b` has to be computed. which is `d` muliplications and 1 addition which is in O(d).

f) Q:Ridge regression . . .
1. can be trained by inverting one matrix in addition to a few additions and multipli-
cations.
2. is much more efficient than least squares regression.
3. cannot evaluate the label of a data point with O(d) computations

A: 1. can be trained by inverting one matrix in addition to a few additions and multipli-
cations.

Note: The RR solutin is `w=(X X^T + 1/(2C)I)^-1 X y` i.e. one matrix addition and one multiplication after the inveerse

To 2.: The cost is pretty much the same. The regularization ensures us some protection against overfitting.

To 3.: just as with LSR the label of a point can be computed in d computations using the affine linear function


g) Q: In the k-nearest-neighbour algorithm . . .
1. most computations are done during training.
2. training involves approximately as many computations as testing.
3. most computations are done during testing.

A: 3. most computations are done during testing.

kNN basically does no training at all. 

h) Q: In machine learning, kernels are considered . . .
1. functions that efficiently compute inner products after a mapping.
2. non-linear machine learning algorithms.
3. important for any machine learning algorithm.

A: 1. functions that efficiently compute inner products after a mapping

We called the mapping (into some high dimensional space) phi in the lecture

To 2.: kernels dont make for non-linear machine learning algorithms themselves.

i) Q: A machine learning model is usually . . .
1. a beautiful woman posing in front of machine learning.
2. not worth using in practice due to its complexity.
3. a parametrized function used for prediction.

A: 3. a parametrized function used for prediction.

j) Q: In general a machine learning algorithm . . .
1. can be kernelized.
2. can be used for any problem.
3. can be used to analyze data.

A: 3. can be used to analyze data.

To 1.: A machine learning model does not necessarily need to be kernelizable
