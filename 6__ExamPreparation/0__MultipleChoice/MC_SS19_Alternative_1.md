# Solutions to `MC_SS19_Alternative_1.PNG`

a) Q: Principal component analysis (PCA) is a supervised learning algorithm.

A: False. PCA is a dimensionality reduction method and is unsupervised.
The dimensionality reduced input data in the original space should be as close as possible to the original data.


b) Q: Autoencoders are a non-linear generalization of PCA.

A: True. For a linear Encoder and Decoder (i.e. no hidden layers) that the solutions of PCA and AE are due to the non-enforcement of orthonormality for AE's.
(see 10.3 on autoencoders in the lecture)
[link](https://stats.stackexchange.com/questions/120080/whatre-the-differences-between-pca-and-autoencoder)


c) Q: Cross-validation can be used to tune a hyperparameter.

A: True. A CV has to be run for all suggestions (i.e. different values, or methods) of the hyperparameter.
The resulting avg. accuracy (on the test-sets of course) for all choices of the hyperparameters can be used to choose the best.


d) Q: The “kernel trick” is frequently used to efficiently transform a non-linear learning machine into a linear learning machine

A: False. The other way round.
The “kernel trick” is frequently used to efficiently transform a linear learning machine into a non-linear learning machine.


e) Q: No  matter  which  training  set,  all  kernelized  classifiers  will  obtain  strictly  better training accuracy than any non-kernelized classifiers

A: False. Just consider a binary classification with 2 datapoints which can be perfectly separated (i.e. 100% training accuracy) by a linear hard-margin SVM.
Thus, the kernelized cannot achieve 'strictly better' training accuracy.


f) Q: In  the  last  decade,  artificial  neural  networks  became  very  popular  because  they obtained good results in some tasks that are considered hard for shallow learning methods.

A: True. Especially Deep learning using CNN's for image classification.


g) Q: Optimizing a function through gradient descent can yield a more accurate solution than stochastic gradient descent.  However, stochastic gradient descent often converges  faster  (in  terms  of  execution  time)  than  gradient  descent  to  a  sufficiently good solution.

A: True. SGD only used a subset of the training data to compute the gradient descent (which makes it faster than GD). As long as the gradient direction is approximately correct it can converge to a suitable but not optimal solution (which the GD would yield).


h) Q: Transfer learning permits us to use an ANN trained for multi-classification to cluster unknown classes.

A: True. The (input-)data is fed through the ANN and the activation of the last hidden layer is used as input to a clustering algorithm as k-means. (see 9.2 Non-linear clustering in the lecture)

i) Q: Applying  the  Box-Cox  transformation  to  the  labels  before  training  a  regression algorithm can improve the regression result.

A: True. In case of linear regression the potential nonlinear data can potentially be linearized by the box-cox transformation. In the transformed coord.-system the linear regression might result in better regression results. (see 8.3 non-linear regression in the lecture)

j) Q: The k-means clustering algorithm cannot be kernelized.

A: False. k-means can be kernelized by 1) computing the distance between data and centroid using only kernels and 2) never explicitely computing the centroids.  (see 9.2 non-linear clustering)
