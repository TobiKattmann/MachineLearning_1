# clustering_WS17-18_Alternative_1.PNG

a) Q: Suppose we are running k-means on a collection of data x1,...,xn. Given centers c1,...,cm,
write pseudocode describing one update of centers using the k-means algorithm

A:
```
for i=1:n do
  yi = argmin_{j in 1:m} ||xi - cj||^2
end for
for j=1:m do
  cj = average({xi : yi = j})
end for
```

b) Q: How do we know when to stop running the k-means algorithm?

A: When the cluster centers dont change anymore. Which could be RMS of the distances between old and new cluster centers.
