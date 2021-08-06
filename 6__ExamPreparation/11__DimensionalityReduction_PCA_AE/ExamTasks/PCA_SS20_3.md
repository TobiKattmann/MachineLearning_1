# PCA_SS20_3.PNG 

a) Q: What is the first principle component of the data according to PCA?

A: The diagonalization shown or [Eigendecomposition](https://en.wikipedia.org/wiki/Eigendecomposition_of_a_matrix#Example) is of form `Sn = P D P^-1`.
With P having the EVec in the columns and D having the respective EVal on the diagonal.

To get the first principal component the EVec of the largest EVal is taken `(2.74, [-4,3])`.

The EVec still has to be normalized to have `||w||=1`. That is done by `||EVec||^-1 EVec`.
That results in the 1st PC `[-4/5, 3/5]`

b) Q: Project the point x = [2 −4]T using PCA with k = 1 into the coordinate system with
the basis made up of the first principle component.

A: Therefore one uses `\tilde X = W^T X` where `W^T=[-4/5, 3/5]` in our case.
Then `\tilde X = -4`.

c) Q: What happens to data points if we project them using PCA as in c) but with k = 2?
Illustrate this using a sketch.

A: As the original data has dimension 2 as well the PCA with k=2 will be coordinate transformation without any reconstruction error in the coordinate system with the basis being the 2 principal components.
I.e. some rotation+mirroring of the original coord system.

Again, there was no actual reduction of dimension so the "reduced" data in the original system (called `\hat X` in the lecture) will be exactly the original data.

d) Q: What could the process from d) be used for?

A: ?? Just a nicer view maybe

e) Q: Assume that the Sn above is not centered and we do not have access to the data points.
Can we use the same trick we used to center the kernel matrix to center Sn? Explain your
answer.

A: ?? 
