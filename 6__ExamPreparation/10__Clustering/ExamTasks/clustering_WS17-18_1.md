# clustering_WS17-18_1.PNG

a) Q: a) Given Pseudocode of the k-Means implementation. Find the error in the code.

A: The ending condition is flawed **See clustering_WS17-18_2.md for an explanation**

In line 9 the cluster assignment needs to be done for each datapoint 1 to n oppose to 1 to m.
In line 12 then it is the other way round.

In line 2 it would need to be 1..n not m.

In line 12 the cluster center on the left hand side should be ci not cj (but for consistency one should then swap i and j for that loop)

I think the person who wrote that down introduced several mistakes of his own

b) Q: Describe in detail how you would fix the bug.

A: Swap lines 9 and 12 ... and do the rest as stated above
