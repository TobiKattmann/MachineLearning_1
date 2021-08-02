# clustering_SS20_2.PNG

a) Q: Use the above lines to code k-means. You may use lines twice. Some lines are traps, i.e.
they are not needed

A: 3,6,7,4,5,1,11,10,1,9,2


b) Q: Kernelization means replacing inner products xTi xj with the kernel function k(xi,xj).
However, inner products do not appear in the above k-Means code. How then can k-
Means be kernelized?

A: Introducing the kernel feature map for computing the cluster centers (i.e. the mean over the datapoints that are currently in the cluster)
and for the computation of the distance of each point wrt all cluster centers.

The key construct is that ||phi(xi)-cj||^2 can be written as ||phi(xi)||^2 -2 phi(xi)^T cj + ||cj||^2

From there on the inner products can be written in terms of kernel feature maps which then can be replaced by kernel evaluations.

See the lecture derivation for more.
