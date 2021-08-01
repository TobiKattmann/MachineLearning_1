# MC_WS17-18_Alternative_1.PNG

**Note**: a+b multiple choice and c+d to be answered by hand

a) Q: Which of the following are advantages of neural networks? Check all that apply.

A: The training procedure scales well with large amounts of data.
**Note**: Yes, it pretty much has to because people are throwing enormous datasets on NN

The training procedure is a convex optimization problem
**Note**: Wrong, in general the NN training is not a convex optimization problem. [link](https://stats.stackexchange.com/questions/106334/cost-function-of-neural-network-is-non-convex)

They perform well on some classically difficult machine learning problems.
**Note**: Yes, especially in the field of image recognition. The NN learns a good feature representation, which e.g. (kernel-)SVM do not.

b) Q: A function f : R->R is convex if ...

A: f'' is strictly positive
**Note**: A twice-differentiable function of a single variable is convex if and only if its second derivative is nonnegative on its entire domain. [wikipedia](https://en.wikipedia.org/wiki/Convex_function)
That means f'' can also be zero and does not need to be strictly positive, i.e. the statement `A function f : R->R is convex iff f'' is strictly positive` would be wrong

c) Q: Write down the names of two regression algorithms.

A: Least squares regression (to make it applicable to nonlinear data apply e.g. Box-Cox transformation to data)
Ridge Regression, which is least squares regression with a regularizer (LOOCV which is n-fold-CV can be efficiently applied because only 1 matrix inversion is necessary). Kernel-RR for nonlinear data.
Decision trees (using bagging or random forests for better results).

d) Q: Qualitatively describe the difference between the hard and soft-margin support vector
machine.

A: A hard-margin SVM linearly seperates binary data such that all training points are classified correctly (zero training error). 
The support vectors cannot lie inside the margin, they are always directly on the margin.
The soft-margin error can have a non-zero training error, i.e. wrongly classified data. 
This has the advantage that the solution can better separate majority of points, instead of focussing eventual outliers in the dataset. [link](https://stackoverflow.com/questions/4629505/svm-hard-or-soft-margins/4630731)
The support vectors (which are the only ones that influence the solution) now can lie inside the margin.
