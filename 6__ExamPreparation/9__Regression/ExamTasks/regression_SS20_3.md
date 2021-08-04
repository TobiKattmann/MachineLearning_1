# regression_SS20_3.PNG

a) Q: Derive a closed form solution for wT RR.

A: See Ridge Regression derivation in the lecture. The result is
```
w_TRR = (1/(2C)I + X X^T)^-1 (X y + s)
```

b) Q: The above equation is a slight variation on ridge regression. State the difference between
ridge regression and the above regression, including a geometric interpretation.

A: The term `-s^T w` is new in this variation.
As the term is substracted the optimizer will try to maximize it.
Vector `s` is fixed so the inner product becomes large if `w` shows into the same direction as `s` (meaning of the inner product), and/or `w` becomes large.
The second requirement is at odds with the first term in RR `1/2||w||^2` which suggests minimizing `w`.

This can be resolved with the following (adding zero):
```
1/2||w||^2 - s^T w + 1/2||s||^2 - 1/2||s||^2
1/2||w - s||^2 - 1/2||s||^2
```
which results in a the following opt problem
```
w_TRR = argmin_w 1/2||w - s||^2 + C||y - X^T w||^2 - 1/2||s||^2
```
where we could also get rid of the constant last term as it wont change the optimal solution for w
```
w_TRR = argmin_w 1/2||w - s||^2 + C||y - X^T w||^2
```
Not the first term becomes minimal when s=w without a competing (contradicting) term.
