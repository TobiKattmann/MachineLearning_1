# SVM_SS19_3.PNG 

**Note**: The square operator has to wrap the max function and not the inner one! Otherwise the max operation can always choose the right term as a value squared is always >= zero. See also  SVM_SS19_4.PNG. 

a) Q: Compte gradient of squared hinge loss.

A: Of the first term just `w` of course
And for each of the entries i of the second term a distinction has to be made.
The gradient is zero if yi(w^T xi) >= 1.
The gradient elsewise is: -2C yi xi (1-yi(w^T xi)).

b) Q: How that the SVM using the squared hinge loss is also a convex problem.

A: From the lecture the following is known:
- An unconstrained optimization problem of the form min_{x \in R^d} f(x) is convex if f is a convex function
- If f, g are convex functions, then f+g is convex
- Let c>0 a scalar and f convex, then cf is convex
- A matrix is positive semi-definite if a^T M a >= 0 for all a \in R^n

The first term of f 0.5||w||^2 is convex. (The Hessian is a unit matrix and thus  a^T I a = a^T a = ||a||^2 >= 0 for all a)

And for each of the entries i of the second term a distinction has to be made.
The function is zero if yi(w^T xi) >= 1, and it is known that each linear function is convex. Zero is a linear function (even a constant one) and this convex.

Elsewise the derivation is a bit trickier.
Building the Hessian H_w (f) for that partmeans to differentiate -2C yi xi (1-yi(w^T xi)) wrt w again.
Which simplifies to taking differentiate +2C yi^2 xi (w^T xi). 
Note that yi^2 in binary classification yi \in {+1,-1} is always 1.
Thus the term +2C xi (w^T xi) is left to differentiate, which is the matrix 2C (xim*xin)_{m,n \in {1..d}}.
That matrix (the Hessian) can be written as 2C xi xi^T.
Putting that into the definition of positive semi-definitness a^T (2C xi xi^T) a = 2C (a^T xi) ( xi^T a) = (a^T xi)^2 >= 0 (which was to be shown)
Thus the SVM using the squared hinge loss is a convex OP.

c) Q: Why is it important for machine learning problems to know if a function is convex?

A: A convex function only has one minimum which is by definition the global minimum.
Thus a Gradient Descent will find the global minimum and will not 'get stuck' in intermediate non-global miinima.
In order to show that an OP is convex it needs to be shown that the objective and inequality constraints are convex functions.

d) Q: Consider the hard-margin SVM as introduced in our lectures (using the standard hinge loss, not the squared hinge loss), and consider the following binary classification problem:
`image` Can we solve this problem with hard-margin SVM? Justify your answer.

A: No, this problem cannot be solved using hard margin SVM. The outlier of class -1 in the +1 cluster prevents that the two clusters are linearly seperable.
  
e) Q:  Put C=1 in Equation (1). Let H1 be the hyperplane that is the solution
of (1) when using the hinge loss. Analogously, let H2 be the hyperplane that is the
solution of (1) when using the squared hinge loss. Draw two hyperplanes H1 and
H2 into Figure 3. Do not forget to label the two lines with H1 and H2, respectively.
Explain your decision.

A: The squared hinge loss will penalize outliers (wrong classified and far away from decision boundary) more than the hinge loss, due to the squaring operation.
Therfore I suspect, that H2 will be closer to the +1 cluster with the outler than H1. I.e. make H1 separate the datasets and make H2 a more towards the +1 dataset.
I am not sure whether H2 should be parallel or slighlty angeled such that it cuts H1 in the top left corner of the image.

