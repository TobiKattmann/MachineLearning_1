# CNN_SS19_3.PNG 

a) Q: Convolutional Neural Networks (CNN) are broadly used in computer
vision tasks. The concepts of patch, stride and pooling are very important in
this context. Write down pseudocode that implements max pooling. Consider
as input to your algorithm the following items: an 8-bit gray scale image ma-
trix M ∈ {0,1,2 ...,255}p×p (i.e., feature entries in {0,1,2,...,255}), a stride of
s (0 < s ∈ N) and a patch size of m ×m, where 0 < m ∈ N. An example of the
matrix M (where p = 7) can be seen in Figure 4. Your output is a 8-bit gray scale
image matrix Mpool ∈{0,1,2 ...,255}d×d.

A: 
```
maxPooling(stride s, image M, imagesize p, patchsize m)
Compute output image dimension d=(p-m)/s + 1
for i=0:d-1 do
  for i=0:d-1 do
    A[i,j] = max(M[s*i:s*i+m, s*i:s*i+m])
  end for
end for
return A
```

b) Q: Execute max pooling on the matrix
presented in Figure 4. Your answer must be a matrix

A:
236 | 236 | 196
-|-|-
242 | 240 | 240
242 | 240 | 240

c) Q: Dimensionality reduction is an effective technique
for regularizing shallow learning methods. Suppose you are solving a binary clas-
sification problem through a very deep neural network (consisting of hundreds of
hidden layers). In this scenario, discuss the effectiveness of dimensionality reduction
as a method to avoid overfitting.

A: The dimensionality reduction can be performed by the NN itself in the first layer.
Therefore additional dim-red does not have that big of an impact mmost-likely.
In the lecture it was shown that a linear Encoder of an Autocoder is in the form of PCA.
In the worst case a dimensionality reduction upfront could destroy important features that allow the binary classification.
On the other hand a prior dim-red might denoize the data such that the NN has a much easier task.

[link](https://stats.stackexchange.com/questions/67986/does-neural-networks-based-classification-need-a-dimension-reduction)
