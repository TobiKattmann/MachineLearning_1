# clustering_SS20_3.PNG

a) Q: Use the above lines to code the k nearest neighbor algorithm, this includes the training
as well as the evaluation of k nearest neighbor. You may use lines twice. Some lines are
traps, i.e. they are not needed.

A: 1,9,10,11,13, ---  2,4,7,3,12,5,6,13
```
func train(k, X, y)
  store X
  store y
  store k
end func
```
```
func eval(x)
  init d as empty list
  for i=1:n do
    d.append(d(xi,x),yi)
  end for
  sort d ascending order
  return the vote of d[0:k]
end func
```

b) Q: Prove that KNN can be kernelized.

A: Similar to kernel k-means clustering, without having to replace the cluster centers.
The only time data is involved is the distance computation using the Euclidian Norm:
```
||xi-x|| = (||xi-x||^2)^{1/2}
```
In the following we drop the sqrt because it will change the distance, but not relative to another point (i.e. we will find the same k clostest points)
Now we can write:
```
||xi-x||^2 = ||xi||^2 - 2 xi^T x + ||x||^2 = xi^T xi - 2 xi^T x + x^T x
```
Now the distance computation is formulated in terms of inner products only so we can apply the kernel trick (i.e. replacing inner products by the kernel, which represents the inner product in a potential high dimensional space).
```
xi^T xi - 2 xi^T x + x^T x = k(xi,xi) - 2 k(xi,x) + k(x,x)
```
With that kNN was succesfully kernelized

c) Q: How does changing k relate to underfitting and overfitting. Explain your answer

A: Increasing k can lead to underfitting and decreasing k can lead to overfitting.
In the limit of increasing k (i.e. k=number datapoints) one would always classify for the label that has the most datapoints. Which is certainly underfitting.
In the limit k=1, one of courses only searches the one nearest neigbor. That can result in a super fragemented decision boundary that is highly sensitive to changes in the input data.

d) Q: KNN is sometimes called an unusual ML algorithm as evaluation computationally takes
more time than training. Explain why this is unusual.

A: In many other ML algos we use large datasets to train a classifier.
This classifier has a number of Degrees of Freedom which we modify such that they best solve our problem.
These DOF's are modified in an iterative manner (often in some Gradient descent) until the optimizer stops.
