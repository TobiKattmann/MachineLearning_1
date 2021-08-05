# Kernel_SS20_3.PNG

a) Q: Prove that k(x,x′) := k1(x,x′)k2(x,x′) is a kernel

A: See excercise sheet 4 1)d. Basically the kernel feature map is the matrix of combination between the 2 feature maps, but written underneath in a vector.
The resulting feature map will map into the space that is of dimension (dim of 1st feature map)*(dim 2nd feature map)

b) Q: Prove that the polynomial kernel, k(x,x′) := (xT x′ + c)p is a kernel

A: See excercise sheet 4 2).
But in short `x^T x` is a kernel (symmetric, with identity as kernel feature map).
A constant is a kernel (symmetric, with sqrt(constant) as kernel feature map).
The sum of two kernels is a kernel (see exc 4 1)c, there note that the resulting kernel feature map is the concatenation of both, i.e. the dimension add up)
And for the exponent one can inductively apply task a) above to show that it is a kernel

c) Q: Consider the feature map φ : Rd →Rm for the polynomial kernel, such that (xT x′+ c)p =
〈φ(x),φ(x′)〉. Explicitly derive the formula for m involving d and p

A: First of all I think the task is not formulated correctly because we can always make the kernel feature map bigger without changing its intent.
Adding zeros will have that kernel feature map remain valid bit it becomes larger in dimensions.
In case one finds a kernel feature map one cannot be sure that there doesn't exist a kfm in lower dimensions.

That said one can derive a (not the) formula for m by applying what we know from the proofs above.
Adding two kernel adds its dimensions and multiplying multiplies them. 
The kernel feature map of identity has size d (as it is just identity) and the kernel feature map of a constant has size 1.
Therefore the addition has d+1 as size.
Now for the addition we multiply p times so we have (d+1)^p as (possible) kernel feature map size.

d) Q: Explain why knowing the dimensionality of a feature map for a kernel might be helpful.

A: From the lecture we know that d+1 points can be linearly seperated in a d-dimensional space.
We cannot guarantee that for d+2 points in a d-dim space.
So, knowing that the feature map is in a higher dimensional space than we have datapoints guarantees that the data is linearly sperable in that space.
(On the other hand i guess having too many unnecessary dimension can also result in overfitting)
