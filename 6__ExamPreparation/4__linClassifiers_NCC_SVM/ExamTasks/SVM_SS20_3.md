# SVM_SS20_3.md

a) Q: State the objective function of the soft-margin SVM, using the hinge-loss.

A:
```
J = 1/2||w||^2 + C sum_i=1^n max(0, 1- yi(w^t xi + b))
```

b) Q: State what property has to hold for a vector to be a support vector.

A: From lecture 2.2 (3) we have:
All vectors xi with `yi d(xi, H(w^*,b^*)) < gamma^*` are called support vectors. 
With d being the signed distance function and gamma the margin.
For the proof, that SVM is a convex OP  we used that `gamma = 1/||w||`.
The signed distance is computed via `d=1/||w|| (w^T x + b)` (see. 2.1 (1)).

Thus for a vector x to be a support vector it must hold that:
```
yi/||w|| (w^T x + b) <= 1/||w|| => yi (w^T x + b) <= 1
```
which basically translates to: The hinge loss must not evaluate to zero for that vector.
That makes sense: As long as some point/vector has a loss it will contribute to the solution.

[link](https://math.stackexchange.com/questions/1305925/why-is-the-svm-margin-equal-to-frac2-mathbfw)

c) Q: Consider the case where C = 0, state an optimal w and b and state the number of support
vectors.

A: When C=0 then the obj func is
```
J = 1/2||w||^2
```
which is not dependend on any datapoints. Thus the solution to that opt problem is w=0 and b \in R (can be chosen freely).
From a logical sense there are no support vectors as the solutiion does not depend on any datapoint.

d) Q: Consider the case where C → ∞, state an optimal w and b and state the number of
support vectors

A: When C-> inf then the soft margin SVM solution degenerates against the hard margin solution.
In this case on can geometrically see that by drawing the points from the task. The decision is then of course at `x=-1/2`.
From that we can put up the equation for the hyperplane `w^T (-1/2) + b = 0`. 
But now we have 1 equation and two unkowns. 
We also know from the problem that the margin gamma is `1/2`, with `gamma = 1/||w||` we have `1/2 = 1/||w||`.
Because in hard margin we the support vectors lie on the margin (i.e. we have 2).
Where in this scalar case `||w||=|w|`.
Now we have a second equation. But from the second equation we have `w= +- 2`.
That gives the possible solutions `w=2 and b=1` or `w=-2 and b=-1`
From checking with any point with the `yi(w^T xi + b) >= 0` as the requirement we know that `w=-2 and b=-1` is the solution.
