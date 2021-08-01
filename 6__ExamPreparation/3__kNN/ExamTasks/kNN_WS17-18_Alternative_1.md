# kNN_WS17-18_Alternative_1.PNG

a) Q: In a binary classification setting, why is the k-nearest neighbors classification algorithm a bit simpler when k is chosen to be odd?

A: Because is the majority-vote between the k nearest neighbors will always provide a clear winner. With even k a tie can occur, which requires a tie-breaker.

b) Q: Let (x1,y1) ,...,(xn,yn) be some classification data. Given a test point xt, write pseudo-code for predicting the test label yt using the k-nearest neighbors algorithm.

A:

1: Input: {(x1,y1) ,...,(xn,yn)}, k, xt

2: Compute distances of xt to the training points e.g. in the euclidian norm ||xi-xt||_2

2: Find k points in the input data that are closest to xt

3: Assign yt to majority vote (with some tie-breaker for even k) of the labels of the k closest points found in the previous step

4: return yt
