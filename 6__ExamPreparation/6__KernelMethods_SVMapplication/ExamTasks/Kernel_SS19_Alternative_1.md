# Kernel_SS19_Alternative_1.PNG

a) Q: Give, with a brief justification, two scenarios where
it is not beneficial to use a kernel method

A:
1. When the number of data points n is very high the kernel matrix is prohibitively large to be stored in memory (n^2)
2. The data is always linearly seperable if n <= d+1 



b) Q: If we are given n datapoints x1,x2,...,xn and a kernel function k(x,  ̃x),
define the corresponding kernel matrix K ∈Rn×n. Prove that K is positive semidef-
inite

A: We will express K in terms of a matrix-matrix product.
Let A be the matrix with the row vectors being ph(xi). 
Then K = A A^T.
Inserting that into the def of pos semi-defintiness then

a^T (A A^T) a >= 0 for a being a vector in R^n (n: number of datapoints)

a^T (A A^T) a = (a^T A)(A^T a)

Now say b := A^T a then b^T = a^T A and

(a^T A)(A^T a) = b^T b = ||b||^2 >= 0

which is what to be proved.


c) Q: Let X be a matrix where the entries are natural numbers between 1
and m (X ∈ {1,2,3,...,m}d×n), m >> 0, d is the number of features and n is the
number of data points (n >> 0) . Let also K ∈ Rn×n be the kernel matrix defined
by Ki,j = k(X.,i,X.,j ), where k : Rd ×Rd → Ris the kernel function and ∀l, X.,l
is the lth column of X.
What is the lowest value of n that guarantees the kernel matrix K is singular (not
invertible) for any matrix X and for any kernel function k? You must justify (prove)
your answer

A: ??

