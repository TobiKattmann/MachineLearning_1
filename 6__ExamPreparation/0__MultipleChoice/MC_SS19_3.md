# Solutions to `MC_SS10_3.PNG` 

a) Q: The k-means algorithm solves the clustering dilemma (that is, finding the right number of clusters).

A: False. The number of cluster `k` has to be given a priori to the k-means algorithm. 

b) Q: k-means is a supervised learning algorithm.

A: False. k-means is a clustering algorithm that tries to partition a set of points in to `k` sets/clusters such that the points in each cluster tend to be near each other.
It is unsupervised because the points have no external classification. [link](https://stats.stackexchange.com/questions/56500/what-are-the-main-differences-between-k-means-and-k-nearest-neighbours)

c) Q: Despite the recent progress in deep learning, SVMs are the state of the art in several applications.

A: True. [link1](https://ai.stackexchange.com/questions/11953/what-are-the-domains-where-svms-are-still-state-of-the-art) [link2](https://datascience.stackexchange.com/questions/711/are-support-vector-machines-still-considered-state-of-the-art-in-their-niche)

d) Q: Cross-validation can be used to compare different algorithms on the same task.

A: False. Cross-validation (CV) can be used to give compare different sets of hyperparameters. (see 8.2 LOOCV in the lecture)
Or, in the first place, CV is used to compute the average classification error and standard deviation of a specific ML-model, as a single training plus testset-run can be misleading. (see 1.1 Motivation and introduction in the lecture)

e) Q: Backpropagation is an algorithm used to regularize an artificial neural network.

A: False. Backpropagation is used to efficiently compute gradients to train an ANN. (or see MC_SS20_2.md, as the question is there multiple choice)

f) Q: The  concept  of  learning  rate  gives  stochastic  gradient  descent  an  advantage  over gradient descent.

A: False. The concept of learning rate applies to both, Gradient Descent and Stochastic gradient descent.
In stochastic gradient descent a higher evaluation speed is traded against gradient accuracy by computing the gradient based on a subset of the training samples instead of all in classic gradient Descent.

e) Q: It is not possible to use an artificial neural network to solve unsupervised tasks.

A: False. For example Autoencoders (AE) in non-linear dimesnionality reduction (i.e. training an ANN to first encode/code the data to lower dimension and then decode/reconstruct the input data as good as possible).
Or Transfer Learning with clustering (i.e. Clustering on the output/last-hidden-layer of a pretrained ANN). [link](https://stats.stackexchange.com/questions/140148/how-can-an-artificial-neural-network-ann-be-used-for-unsupervised-clustering)

h) Q: No matter which learning problem, reducing the dimensionality of the data matrix results in a loss of relevant information and thus increases the root mean squared error (RMSE).

A: False. The dimensionality reduction might cause no loss of relevant information (e.g. if the reduced dimension was exactly the same for all data points).
What is the RMSE applied to in e.g. binary classification? (I would say that is not uniquely defined.) The most/(only?) straight forward application of RSME is for regression.

i) Q: Early stopping can be used to regularize an artificial neural network.

A: True. (see. 7.4 Regularization for deep learning). 
Split training set into smaller training set + validation set. Monitor the validation error every couple of minibatch SGD iterations. Stop SGD optimization early when validatione error goes up.

j) Q: Most linear classifiers can be kernelized. However, up to now, not a single kernelized regression algorithm is known.

A: False. For example kernel Ridge-regression (KRR) by applying the kernel-trick and the representer theorem. (see 8.3 Nonlinear Regression in the lecture)
