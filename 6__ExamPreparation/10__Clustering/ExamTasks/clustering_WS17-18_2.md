# clustering_WS17-18_2.PNG 

a) Q: Find error in k-means pseudo code

A: The exit condition of the algorithm is flawed such that it will only run 1 iteration.
In line 15 ci' is set to ci and in 17 the check ci'= ci will always be true. 

In line 9 the original k-means take the squared distance instead of the plain distance which is used here.
The resulting cluster centers will be exactly the same as the square function is strictly monotone increasing, thus preserving relative distances.
That means, if j* is the closest cluster center in the plain norm, j* will be the closest cluster center in the square norm as well.

For completeness one might nag about line 9 that one should specify the argmin as being over j \in {1,..,m}

b) Q: Precisely describe how to fix the algorithm to correctly implement k-means.

A: Move lines 14-16 directly after the `repeat` line 7.
Like so, the old cluster centers are stored into ci', then the new ones are computed.
And then in the `until` statement the old and news ones are correctly compared.

In line 9 replace ||.|| by ||.||^2
