# SVM_SS20_1.PNG 

a) 

A:
```
J = 1/2 ||w||^2 + C sum_{i=1}^n max(0, 1-yi(w^t xi + b))
```

b) Q: 

A:
The GD algo is
```
(w_i+1,b_i+1) = (w_i,b_i) - lambda grad_{w,b} J
```
with the gradient
```
grad_w J = w + C sum_{i=1}^n {-yi xi if yi(w^t xi + b)<1 ; 0 elsewise}
grad_b J = C sum_{i=1}^n {-yi if yi(w^t xi + b)<1 ; 0 elsewise}
```
Now one just has to compute. In the first iteration `yi(w^t xi + b)<1` is true for all datapoints.
`w1 = [-1/2, 0]^T` and `b1 = +1`

In the next iteration only the 3rd and fourth datapoint have `yi(w^t xi + b)<1` (the first and second are 1) so that needs be taken care of!
The gradient descent step results in the same solution `w1 = [-1/2, 0]^T` and `b1 = +1`.
Thus the algo converged.

c) Q: 

A:
The hyperplane is given by `w^t x + b = 0` which results in `x1=2` i.e. the result is the the line parallel to x2 at x1=2.

Two points (which of course also define a line and can be chosen arbitrarily) are e.g. [2,0] and [2,1]

d) Q: 

A:
The classification is done using `sign(w^t x + b)` where `w^t x + b=3/4 > 0` with `x=[1/2,0]` i.e. the label of the datapoint is +1.

This can also be plausibilised by drawing the points and the hyperplane
