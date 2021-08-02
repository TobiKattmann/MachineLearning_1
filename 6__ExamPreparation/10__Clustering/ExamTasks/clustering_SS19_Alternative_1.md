# clustering_SS19_Alternative_1.PNG

a) Q: Draw into Figure 2 reasonable centroids that could result from running the k-means
algorithm until convergence, using k = 3

A: {G K H C} {I B A}{E D J F} straight forward

b) Q: A disadvantage of the k-means algorithm is that we need to define the
number of clusters before its execution. One way to solve this problem is by using
hierarchical clustering. Based on the data shown in Figure 2, draw the resulting
tree of clusters by performing average linkage hierarchical clustering

A: In hierarchical clustering, each node at the start is a cluster center.
Then the two clusters (out of all possible) with the minimal distance are linked to form a new cluster.
This process is then repeated until a single root is left.
Computing the distance between different clusters can be done via simple, average or complete linkage.

That said. I think the clusters are formed like follows:
{D J}{K C}{I B}{G H} which are somewhat straight forward.
Then {D J E}{I A B}{G H K C}.
Then {D J E F}.
Then the right two big {I A B E D J F}
And finally all nodes.

c) Q: In clustering tasks involving very high-dimensional
inputs, would it be advantageous to first apply PCA before running the k-means
algorithm (on the dimensionality-reduced data)? Why?

A: Yes, in case there is number of pricipal components that explain the majority of the variance of the dataset, then doing PCA before clustering will most likely retain the original cluster structure.
The advantage is that in the lower reduced space after the PCA it computationally less expenisve to compute the distances between datapoints.
[link](https://www.quora.com/Should-I-use-PCA-as-a-preprocessing-step-to-k-means-clustering)
